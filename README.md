# Gcore Api

## 说明

API从客户端中扒出来的。

准备用该API写个Flutter App玩玩。仅此而已。



***以下没有特殊说明的均为GET***

## 分类

### 分类列表

 **api/categories**

```json
{
    "status": 1,
    "results": [
        {
            "id": 2,
            "name": "新闻",
            "desc": "",
            "show_name": "资讯",
            "type": "Column",
            "specific_type": "news",
            "logo_url": "https://image.gcores.com/cd39cf6f-b918-4676-9000-994dd271abb5.png",
            "background_url": "https://image.gcores.com/c6116099-58cb-4c99-888d-c4dd895d464c.jpg",
            "subscriptors_num": 13854,
            "originals_num": 8955
        }
    ]
}
```



### 分类信息

**api/categories/{id}**

| 参数 | 说明   |
| ---- | ------ |
| id   | 分类id |

```json
{
    "status": 1,
    "results": {
        "id": 2,
        "name": "新闻",
        "desc": "",
        "show_name": "资讯",
        "type": "Column",
        "specific_type": "news",
        "logo_url": "https://image.gcores.com/cd39cf6f-b918-4676-9000-994dd271abb5.png",
        "background_url": "https://image.gcores.com/c6116099-58cb-4c99-888d-c4dd895d464c.jpg",
        "subscriptors_num": 13855,
        "originals_num": 8955,
        "is_subscript": false
    }
}
```





## 文章

### 某分类下的列表

**api/categories/{id}/originals**

| 参数 | 意义   | 取值           |
| ---- | ------ | -------------- |
| id   | 分类id | 1: 新闻 9:电台 |
| page | 分页数 |                |

```json
{
    "status": 1,
    "results": [
        {
            "id": 106078,
            "type": "Volume",
            "title": "《王国之心》故事06：决战之前最后的梦境",
            "desc": "《王国之心：梦中降生》与《王国之心 梦降深处》的故事",
            "thumb_url": "https://image.gcores.com/37a2c0d2-4a79-4a17-b21c-35c6e4d93bde.jpg?x-oss-process=style/original_hsat2x",
            "cover_url": "https://image.gcores.com/76a54e04-34de-458f-adc6-179f8208cfb5.jpg",
            "permalink": "https://www.gcores.com/originals/106078",
            "vol": "44",
            "likes_num": 28,
            "comments_num": 46,
            "created_at": "2019-02-02 00:00:00",
            "timellines_images_url": "https://alioss.gcores.com/timelines_images/106078-1549035540.zip",
            "duration": 4692,
            "user": {
                "id": 385,
                "nickname": "Hardy",
                "thumb_url": "https://alioss.gcores.com/uploads/user/ee2a192c-983d-4985-9939-7c1cdcaa779e_normal.jpg",
                "location": "北京",
                "is_fresh": false
            },
            "category": {
                "id": 53,
                "name": "Gadio Story",
                "desc": "",
                "show_name": "Gadio Story",
                "type": "Show",
                "specific_type": "audio",
                "logo_url": "https://image.gcores.com/1e3bcc5f-923f-4188-84c2-2f97cc7a3a38.png",
                "background_url": "https://image.gcores.com/83c591f3-f3a4-4326-a6a8-57bda3500bae.png",
                "subscriptors_num": 11566
            },
            "media": {
                "mp3": [
                    "https://alioss.gcores.com/uploads/audio/7658b9a0-d2f2-4d21-85de-a9b776d79b5e.mp3"
                ]
            }
        }
    ]
}
```



### 首页文章列表

**api/originals/home**

```json
{
  "status": 1,
  "results": [{
    "type": "original",
    "data": {
      "id": 105946,
      "type": "Article",
      "title": "少了满嘴荤段子与血腥特效的《死侍2》终成一部“家庭片”",
      "desc": "这样的和谐手法，简直比原来“搞笑”多了！",
      "thumb_url": "https://image.gcores.com/b638d8ca-c0ce-4b5a-90a1-fde662e2ec59.jpg?x-oss-process=style/original_hsat2x",
      "cover_url": "https://image.gcores.com/9e47b286-ad76-4caf-8553-f5e6b4570724.jpg",
      "permalink": "https://www.gcores.com/originals/105946",
      "vol": null,
      "likes_num": 2,
      "comments_num": 2,
      "created_at": "2019-02-02 12:01:15",
      "user": {
        "id": 284117,
        "nickname": "漫威未来之战",
        "thumb_url": "https://alioss.gcores.com/uploads/user/3d2ed4b6-8cdc-4bc7-bd96-7567d6b5b29c_normal.jpg",
        "location": "广东省",
        "is_fresh": false
      },
      "category": {
        "id": 56,
        "name": "有感而发",
        "desc": "",
        "show_name": "有感而发",
        "type": "Column",
        "specific_type": "article",
        "logo_url": "https://image.gcores.com/e15bb518-393d-4f9e-9214-6229aaece5a7.png",
        "background_url": null,
        "subscriptors_num": 299
      }
    }
  }]
  m
```



### 文章详情

**api/originals/{id}**

| 参数 | 说明   |
| ---- | ------ |
| id   | 文章id |



## 评论

### 获取单条评论

**api/comment/{id}**

| 参数 | 说明   |
| ---- | ------ |
| id   | 评论id |





### 评论列表

**api/comments**

| 参数             | 说明                        |
| ---------------- | --------------------------- |
| commentable_type | 文章类型，取值为 'original' |
| commentable_id   | 文章id                      |
| page             | 页数，从0开始               |
| sort             | 排序，取值为 'hot'          |

```json
{
  "status": 1,
  "results": [{
    "id": 1351138,
    "body": "文化隔离…以至于诞生出了新的艺术变体。",
    "created_at": "2019-02-02 12:14:28",
    "likes_num": 7,
    "user": {
      "id": 81939,
      "nickname": "歧文公",
      "thumb_url": "https://alioss.gcores.com/uploads/user/7c665c41-3fc1-4e18-a055-96e1a6356bdc_normal.jpg",
      "location": "",
      "is_fresh": false
    },
    "to_user": null
  }]
}
```



## 账号

### 登录

POST **auth/identity/callback**

| 参数       | 说明             |
| ---------- | ---------------- |
| auth_key   | 用户名/手机号 等 |
| password   | 密码             |
| sourceType | 取值为'app'      |



```json
{
    "status": 1,
    "results": {
        "auth_token": "XXXXXXXXXXXXXXXXX",
        "user": {
            "id": 287123,
            "nickname": "XXXXXX",
            "thumb_url": "https://alioss.gcores.com/default_thumb/user-normal.png",
            "location": "",
            "is_fresh": false,
            "providers": [
                "identity"
            ],
            "is_staff": false
        }
    }
}
```



## 其他

### 首页走马灯

**api/originals/home_slideshow**

```json
{
    "status": 1,
    "results": [
        {
            "image": "https://alioss.gcores.com/uploads/mobile_app_focus_image/7d37f83c-d46b-45de-b271-e570d9d65500.jpg",
            "original_id": 106078,
            "original_type": "Radio"
        },
        {
            "image": "https://alioss.gcores.com/uploads/mobile_app_focus_image/f51ef596-a100-42ce-a150-a869bea10142.jpg",
            "original_id": 105962,
            "original_type": "Radio"
        },
        {
            "image": "https://alioss.gcores.com/uploads/mobile_app_focus_image/65757b84-c4f3-4945-935f-56785404b09d.jpg",
            "original_id": 105974,
            "original_type": "Video"
        }
    ]
}
```



 