# Api

## rest-api 参考
http://www.ruanyifeng.com/blog/2014/05/restful_api.html

## 首页

### 接口

| url |    https://api.example.com/v1/home.json     |
| ------------- | ----------- |
| HTTP方法    | get |
| 返回格式     | json    |

### 参数

  无

### 返回结果

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| id   | int | false | 专辑ID |
| name | String | false | 专辑名称 |
| poster | String | false | 专辑海报 |
| backgroundPoster | String | false | 专辑大海报当背景 |
| directors | String | false | 导演 |
| actors | String | false | 演员 |
| host | String | true | 主持人 |
| tv_station | String | true | 电视台 |
| rating | String | false | 评分 |
| genre | String | false | 类型， 多个用逗号分隔 |
| episode_count | int | false | 总剧集 |
| episode_updated | int | true | 更新至 |
| view_count | int | false | 总播放次数 |
| area | int | false | 地区 |
| category | string | false | 分类 电视剧 电影 |
| episode_count | int | false | 总剧集 |
| episodes | array | false | 剧集数组 |
| released | string | false | 节目发行时间 (YYYY-MM-DD) |
| state | string | false | 节目状态: normal - 正常 limited - 分级 check - 待审 checking- 审核 blocked - 屏蔽 deleted - 删除 delayed - 延审 paycheck-付费待审 |
| copyright_status | string | false | 节目授权状态 auchorized 已授权 public 公共版权 falseauth 伪授权 unknow 版权未知 expired 版权过期 unauthorized 无版权 |

### json

```json
[
  {
     "id": "834adfc2368f11e1b52a",
     "name": "宫锁珠帘",
     "alias": [
       {
         "type": "0",
         "alias": "宫2"
       },
       {
         "type": "0",
         "alias": "宫锁心玉2"
       },
       {
         "type": "1",
         "alias": "The Palace"
       }
     ],
     "link": "http://www.youku.com/show_page/id_z834adfc2368f11e1b52a.html",
     "play_link": "http://v.youku.com/v_show/id_XMzQ0ODQ4MzU2.html",
     "poster": "http://res.mfs.ykimg.com/050D00004FB317B60000015BB40555AE",
     "thumbnail": "http://g4.ykimg.com/0102641F464F14DBC4000000000000EED795E3-03F6-60B6-2F19-0301E4B671CF",
     "streamtypes": [
       "hd2",
       "flvhd",
       "hd",
       "3gphd"
     ],
     "genre": "剧情,古装,言情",
     "area": "大陆",
     "completed": 1,
     "episode_count": "37",
     "episode_updated": "37",
     "view_count": "188875880",
     "score": "7.985",
     "paid": 0,
     "published": "2012-01-20",
     "released": "2012-01-20",
     "category": "电视剧",
     "description": "雍正年间，候补四品典仪凌柱之女怜儿为父请命结识十七王爷胤礼，二人两情依依，本要结为夫妇，没想到胤礼为救老师阿灵阿，不得已娶了阿灵阿之女嘉嘉为妻，伤心欲绝的怜儿在深宫里步步为营，渴望能走出深宫过平凡的日子，不想却被宫中各股势力所利用，李卫要跟她结盟，大太监苏培盛要向她报恩，亲如姐妹的玉漱出卖她，表面和谐的深宫里埋藏着各种秘密，就在怜儿快喘不过气时，她意外地被雍正看中，成为了万千宠爱于一身的熹妃，而就在这时，她忽然发现所有的事情一下子都变复杂了，停下来就会被迫害，走下去可能连自己也不认识自己了，在三岔路口，她选择了相信阳光，相信暴风雨总会过去的，于是在她坚忍不拔的努力下，终于为自己闯出了一片天。",
     "rank": "0",
     "view_yesterday_count": "0",
     "view_week_count": "291406",
     "comment_count": "88272",
     "favorite_count": "7160",
     "up_count": "581262",
     "down_count": "125799",
     "attr": {
       "director": [
         {
           "id": "16924",
           "name": "李慧珠",
           "link": "http://www.youku.com/star_page/uid_UNjc2OTY=.html"
         }
       ],
       "performer": [
         {
           "id": "22017",
           "name": "杜淳",
           "character": "胤礼",
           "link": "http://www.youku.com/star_page/uid_UODgwNjg=.html"
         },
         {
           "id": "331783",
           "name": "何晟铭",
           "character": "雍正",
           "link": "http://www.youku.com/star_page/uid_UMTMyNzEzMg==.html"
         },
         {
           "id": "382806",
           "name": "袁姗姗",
           "character": "怜儿",
           "link": "http://www.youku.com/star_page/uid_UMTUzMTIyNA==.html"
         },
         {
           "id": "23163",
           "name": "张嘉倪",
           "character": "玉漱",
           "link": "http://www.youku.com/star_page/uid_UOTI2NTI=.html"
         },
         {
           "id": "16669",
           "name": "舒畅",
           "character": "海棠",
           "link": "http://www.youku.com/star_page/uid_UNjY2NzY=.html"
         }
       ],
       "screenwriter": [
         {
           "id": "322397",
           "name": "于正",
           "link": "http://www.youku.com/star_page/uid_UMTI4OTU4OA==.html"
         }
       ],
       "starring": null,
       "producer": null,
       "original": null
     }
   }
]
```

## 根据分类获取节目

### 接口

| url |    https://api.example.com/v1/category.json/     |
| ------------- | ----------- |
| HTTP方法    | get |
| 返回格式     | json    |

### 参数

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| category   | string | false | 分类 电视剧，电影 |
| genre | String | false | 类型 古装,言情 |
| area | String | true | 地区 |
| orderby | String | true | 排序 |
| page | int | false | 页数 |
| count | int | false | 页大小 page*count必须小于等于1000 |

### 返回结果

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| id   | int | false | 专辑ID |
| name | String | false | 专辑名称 |
| poster | String | false | 专辑海报 |
| backgroundPoster | String | false | 专辑大海报当背景 |
| directors | String | false | 导演 |
| actors | String | false | 演员 |
| host | String | true | 主持人 |
| tv_station | String | true | 电视台 |
| rating | String | false | 评分 |
| genre | String | false | 类型， 多个用逗号分隔 |
| episode_count | int | false | 总剧集 |
| episode_updated | int | true | 更新至 |
| view_count | int | false | 总播放次数 |
| area | int | false | 地区 |
| category | string | false | 分类 电视剧 电影 |
| episode_count | int | false | 总剧集 |
| released | string | false | 节目发行时间 (YYYY-MM-DD) |
| state | string | false | 节目状态: normal - 正常 limited - 分级 check - 待审 checking- 审核 blocked - 屏蔽 deleted - 删除 delayed - 延审 paycheck-付费待审 |
| copyright_status | string | false | 节目授权状态 auchorized 已授权 public 公共版权 falseauth 伪授权 unknow 版权未知 expired 版权过期 unauthorized 无版权 |

### JSON

```json
{
       "total" : 100,
       "shows" :
       [
           {
               "id" : "2a7260de1faa11e097c0",
               "name" : "裸婚时代",
               "link" : "http://www.youku.com/show_page/id_z2a7260de1faa11e097c0.html",
               "play_link" : "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
               "poster" : "http://g4.ykimg.com/0100641F464E1FC...",
               "thumbnail" : "http://g4.ykimg.com/0100641F464E1FC...",
               "streamtypes" : ["hd2,flvhd,flv,hd,3gp,3gphd"],
               "episode_count" : 30,
               "episode_updated" : 30,
               "view_count" : "345037980",
               "score" : 9.3,
               "paid" : 0,
               "published" : "0000-00-00",
               "released" : "2011-06-11",
           },
           …
       ]
   }
```
