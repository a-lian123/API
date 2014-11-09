# API

万花筒的 API 文档 （未完成）

1. 用户 OAuth 验证

`GET https://api.wehoton.com/oauth/login`

**参数**

| 名称  | 类型  | 描述 |
| :---- |:-----:| ----:|
| client_name| string |**必需** 你在万花筒后台创建开发者应用时填写的应用缩略名
| secret_key | string | **必需** 你在创建应用成功后获得的应用密钥，用于确认你对该应用拥有权限 |
| redirect_uri | string | **可选** 在万花筒后台设置了`redirect_uri`就可以在发起请求忽略这个参数|
