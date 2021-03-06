# Api

## rest-api 参考
http://www.ruanyifeng.com/blog/2014/05/restful_api.html

## 首页

### 接口

| url |    https://api.example.com/v1/home.json     |
| ------------- | ----------- |
| HTTP方法    | get |
| 返回格式     | json |

### 参数

  无

### 返回结果

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| id   | int | false | 专辑ID |
| description | String | false | 简介 |
| name | String | false | 专辑名称 |
| en_name | String | false | 英语专辑名称 |
| isTitle | boolean | false | 是否是专辑级别 |
| type | int | false | 1 电视剧， 2 电影， 3 综艺， 4 直播， 5 应用 ... |
| poster | String | false | 专辑海报 |
| carousel_episodes | array | false | 轮播 |
| backgroundPoster | String | false | 专辑大海报当背景 |
| directors | String | false | 导演 |
| actors | String | false | 演员 |
| host | String | true | 主持人 |
| tv_station | String | true | 电视台 |
| voice | String | true | 配音演员 |
| rating | String | false | 评分 |
| genre | String | false | 类型， 多个用逗号分隔 |
| episode_count | int | false | 总剧集 |
| episode_updated | int | true | 更新至 |
| view_count | int | false | 总播放次数 |
| area | int | false | 地区 |
| category | string | false | 分类 电视剧 电影 |
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
     "en_name": "hh",
     "description": "雍正年间，候补四品典仪凌柱之女怜儿为父请命结识十七王爷胤礼，二人两情依依，本要结为夫妇，没想到胤礼为救老师阿灵阿，不得已娶了阿灵阿之女嘉嘉为妻，伤心欲绝的怜儿在深宫里步步为营，渴望能走出深宫过平凡的日子，不想却被宫中各股势力所利用，李卫要跟她结盟，大太监苏培盛要向她报恩，亲如姐妹的玉漱出卖她，表面和谐的深宫里埋藏着各种秘密，就在怜儿快喘不过气时，她意外地被雍正看中，成为了万千宠爱于一身的熹妃，而就在这时，她忽然发现所有的事情一下子都变复杂了，停下来就会被迫害，走下去可能连自己也不认识自己了，在三岔路口，她选择了相信阳光，相信暴风雨总会过去的，于是在她坚忍不拔的努力下，终于为自己闯出了一片天。",
     "isTitle": true,
     "poster": "http://res.mfs.ykimg.com/050D00004FB317B60000015BB40555AE",
     "carousel_episodes": [
       {
          "id" : "2a7260de1faa11e097c0",
          "name" : "裸婚时代01",
          "description" : "裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代",
          "play_url" : "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
          "poster" : "http://g4.ykimg.com/0100641F464E1FC...",
          "thumbnail" : "http://g4.ykimg.com/0100641F464E1FC...",
          "streamtypes" : ["hd2,flvhd,flv,hd,3gp,3gphd"],
          "view_count" : "345037980",
       },
       {
          "id" : "2a7260de1faa11e097c0",
          "name" : "裸婚时代01",
          "description" : "裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代",
          "play_url" : "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
          "poster" : "http://g4.ykimg.com/0100641F464E1FC...",
          "thumbnail" : "http://g4.ykimg.com/0100641F464E1FC...",
          "streamtypes" : ["hd2,flvhd,flv,hd,3gp,3gphd"],
          "view_count" : "345037980",
       }
       ...
     ],
     "backgroundPoster": "http://res.mfs.ykimg.com/050D00004FB317B60000015BB40555AE",
     "director": "李慧珠",
     "actors": "杜淳、何晟铭、袁姗姗、舒畅",
     "host": "",
     "tv_station": "",
     "rating": "7.985",
     "genre": "剧情,古装,言情",
     "episode_count": "37",
     "episode_updated": "37",
     "view_count": "188875880",
     "area": "大陆",
     "category": "电视剧",
     "published": "2012-01-20",
     "released": "2012-01-20",
     "favorite_count": "7160",
   }
]
```

## 根据专辑Id获取剧集数据

### 接口

| url |    https://api.example.com/v1/category.json/     |
| ------------- | ----------- |
| HTTP方法    | get |
| 返回格式     | json    |

### 参数

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| titleId   | int | false | 专辑Id |

### 返回结果

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| id   | int | false | 剧集ID |
| name | String | false | 剧集名称 |
| poster | String | false | 剧集海报 |
| description | String | false | 剧集描述 |
| view_count | int | false | 总播放次数 |
| play_url | String | false | 播放地址 |
| streamtypes | String | false | 播放地址类型 |
| thumbnail | String | false | 缩略图 |

### JSON

```json
{
       "total" : 100,
       "shows" :
       [
           {
              "id" : "2a7260de1faa11e097c0",
              "name" : "裸婚时代01",
              "description" : "裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代",
              "play_url" :{
                "l": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
                "m": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
                "h": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html"
              } ,
              "poster" : "http://g4.ykimg.com/0100641F464E1FC...",
              "thumbnail" : "http://g4.ykimg.com/0100641F464E1FC...",
              "streamtypes" : ["hd2,flvhd,flv,hd,3gp,3gphd"],
              "view_count" : "345037980",
           },
           {
              "id" : "2a7260de1faa11e023er",
              "name" : "裸婚时代02",
              "description" : "裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代",
              "play_url" :{
                "l": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
                "m": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
                "h": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html"
              } ,
              "poster" : "http://g4.ykimg.com/0100641F464E1FC...",
              "thumbnail" : "http://g4.ykimg.com/0100641F464E1FC...",
              "streamtypes" : ["hd2,flvhd,flv,hd,3gp,3gphd"],
              "view_count" : "345037980",
           },
           …
       ]
   }
```

## 根据剧集Id获取单个剧集信息

### 接口

| url |    https://api.example.com/v1/episodes.json/     |
| ------------- | ----------- |
| HTTP方法    | get |
| 返回格式     | json    |

### 参数

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| episodesId   | int | false | 剧集Id |

### 返回结果

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| id   | int | false | 剧集ID |
| name | String | false | 剧集名称 |
| poster | String | false | 剧集海报 |
| description | String | false | 剧集描述 |
| view_count | int | false | 总播放次数 |
| play_url | String | false | 播放地址 |
| streamtypes | String | false | 播放地址类型 |
| thumbnail | String | false | 缩略图 |

### JSON

```json
{
   "id" : "2a7260de1faa11e097c0",
   "name" : "裸婚时代",
   "description" : "裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代裸婚时代",
   "play_url" :{
     "l": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
     "m": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html",
     "h": "http://v.youku.com/v_show/id_XMjc0MzM1OTgw.html"
   } ,
   "poster" : "http://g4.ykimg.com/0100641F464E1FC...",
   "thumbnail" : "http://g4.ykimg.com/0100641F464E1FC...",
   "streamtypes" : ["hd2,flvhd,flv,hd,3gp,3gphd"],
   "view_count" : "345037980",
}
```
## 根据频道Id获取频道数据

### 接口

| url |    https://api.example.com/v1/getChannelsById.json/     |
| ------------- | ----------- |
| HTTP方法    | get |
| 返回格式     | json    |

### 参数

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| channelId   | int | false | 专辑Id |

### 返回结果

| 参数  | 类型 | 允许为空 | 说明 |
| :---- |:----:| :-----:| :-----:|
| id   | int | false | 专辑ID |
| description | String | false | 简介 |
| name | String | false | 专辑名称 |
| en_name | String | false | 英语专辑名称 |
| isTitle | boolean | false | 是否是专辑级别 |
| type | int | false | 1 电视剧， 2 电影， 3 综艺， 4 直播， 5 应用 ... |
| poster | String | false | 专辑海报 |
| carousel_episodes | array | false | 轮播 |
| backgroundPoster | String | false | 专辑大海报当背景 |
| directors | String | false | 导演 |
| actors | String | false | 演员 |
| host | String | true | 主持人 |
| tv_station | String | true | 电视台 |
| voice | String | true | 配音演员 |
| rating | String | false | 评分 |
| genre | String | false | 类型， 多个用逗号分隔 |
| episode_count | int | false | 总剧集 |
| episode_updated | int | true | 更新至 |
| view_count | int | false | 总播放次数 |
| area | int | false | 地区 |
| category | string | false | 分类 电视剧 电影 |
| episodes | array | false | 剧集数组 |
| released | string | false | 节目发行时间 (YYYY-MM-DD) |
| state | string | false | 节目状态: normal - 正常 limited - 分级 check - 待审 checking- 审核 blocked - 屏蔽 deleted - 删除 delayed - 延审 paycheck-付费待审 |
| copyright_status | string | false | 节目授权状态 auchorized 已授权 public 公共版权 falseauth 伪授权 unknow 版权未知 expired 版权过期 unauthorized 无版权 |

### JSON

```json
{
  "name": "应用",
  "is_title": false,
  "id": 1234567,
  "en_name": "Application",
  "description": "世纪优优（天津）文化传播股份有限公司（简称：世纪优优；股票名称：世纪优优；股票代码：837666）创办于2012年，是一家全球数字娱乐视频供应商，是中国地区较早开发海外业务、也是目前中国影视推广海外、全球范围内渠道较大的海外全媒体发行运营商。",
  "landscape_poster": null,
  "portrait_poster": null,
  "background_poster": null,
  "masked_background_poster": null,
  "genreListItems": [{
          "id": 1913,
          "name": "甄嬛传",
          "position": 1122416520,
          "source_url": "https://media.w3.org/2010/05/sintel/trailer_hd.mp4",
          "stream_url": null,
          "landscape_poster": null,
          "portrait_poster": "http://7xoboh.com1.z0.glb.clouddn.com/003.png",
          "free": false,
          "livestream": false,
          "description": "世纪优优（天津）文化传播股份有限公司 是一家全球数字娱乐视频供应商，是中国地区较早开发海外业务、也是目前中国影视推广海外、全球范围内渠道较大的海外全媒体发行运营商",
          "background_poster": null,
          "thumbnail": null,
          "blocked_channels": [],
          "blocked_countries": [],
          "thumbnail_interval": 10,
          "masked_background_poster": null
      },
      {
          "id": 1914,
          "name": "琅琊榜",
          "position": 1122416520,
          "source_url": "https://media.w3.org/2010/05/sintel/trailer_hd.mp4",
          "stream_url": null,
          "landscape_poster": null,
          "portrait_poster": "http://7xoboh.com1.z0.glb.clouddn.com/004.png",
          "free": false,
          "livestream": false,
          "description": "世纪优优（天津）文化传播股份有限公司 是一家全球数字娱乐视频供应商，是中国地区较早开发海外业务、也是目前中国影视推广海外、全球范围内渠道较大的海外全媒体发行运营商",
          "background_poster": null,
          "thumbnail": null,
          "blocked_channels": [],
          "blocked_countries": [],
          "thumbnail_interval": 10,
          "masked_background_poster": null
      }
  ]
}

```
