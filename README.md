# API

万花筒的 API 文档 （未完成）

https 暂不可用

| 完成度  | 描述  |
| :---- |:-----|
|★★★★|会增加功能|
|★★★★★|稳定|

## 1. 用户 OAuth 验证

`https://api.wehoton.com/oauth/login`

**参数**

| 名称  | 类型  | 描述 |
| :---- |:-----:| :----|
| client_name| string |**必需** 你在万花筒后台创建开发者应用时填写的应用缩略名
| secret_key | string | **必需** 你在创建应用成功后获得的应用密钥，用于确认你对该应用拥有权限 |
| redirect_uri | string | **可选** 在万花筒后台设置了`redirect_uri`就可以在发起请求忽略这个参数|

**返回内容**

用户登录成功后会跳转到 `redirect_uri/?access_token=string` ，你可以保存 access_token 的内容用于更多的操作。

## 2. 获取话题

**通用的参数** 

| 名称  | 类型  | 描述 |
| :---- |:-----:| :----|
| p | int | **可选** 分页参数，默认为 `1`|
| limit | int | **可选** 一次获取的话题数，默认为 `40` |


### 按时间顺序获取 

完成度 ★★★★

`GET https://api.wehoton.com/topics`

### 按用户ID获取

完成度 ★★★★

`GET https://api.wehoton.com/user/topics/:userID`

### 按节点ID获取

完成度 ★★★★

`GET https://api.wehoton.com/node/topics/:nodeID`

### 获取单个话题

完成度 ★★★★

`GET https://api.wehoton.com/topics/id/:topicID`

## 3. 获取回复

### 获取用户回复

完成度 ★★★★

`GET https://api.wehoton.com/user/replies/:userID`

### 获取话题回复

完成度 ★★★★

`GET https://api.wehoton.com/topics/replies/:topicID`

### 获取单个回复

完成度 ★★★★

`GET https://api.wehoton.com/topics/reply/:replyID`

## 4. 操作话题

### 创建话题

`POST https://api.wehoton.com/topic/new`

### 删除话题

`POST https://api.wehoton.com/topic/delete`

### 编辑话题

`POST https://api.wehoton.com/topic/edit`

### 喜欢话题

`POST https://api.wehoton.com/topic/like`

### 收藏话题

`POST https://api.wehoton.com/topic/favorite`

## 5. 操作回复

### 创建回复

`POST https://api.wehoton.com/reply/add`

### 删除回复

`POST https://api.wehoton.com/reply/delete`

### 编辑回复

`POST https://api.wehoton.com/reply/edit`

