

## 接口定义


### 请求参数说明

- 所有接口均在 headers 头添加 authtoken 字段（登录、注册接口除外），jwt 验证登录有效性


### 返回参数说明

- 返回 json 数据结构示例如下：

```json
{
  "respCode": "10000", //为了简单，这个项目中此字段作用不大
  "respMsg": "operate success", //接口返回提示语句
  "success": 1, //成功为1，失败为0
  "content": {
    "name": "Bob",
    "isOnline": true,
    "age": 18
  }
}
```


### [登录模块](./login_module.md)



- [登录login](./login_module.md#login)
- [注册register](./login_module.md#register)
- [退出登录](./login_module.md#logout)




### [account 模块](./account_module.md)


- [修改 username](./account_module.md#mergeUsername)
- [修改 firstName 和 lastName](./account_module.md#mergeName)
- [修改头像](./account_module.md#mergeAvatar)
- [一次性修改所有个人信息](./account_module.md#mergeEntity)



### [文件模块](./file_module.md)



### [socket io 模块](./socket_io.md)