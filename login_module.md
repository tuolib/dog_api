# 登录接口



## register

- **接口地址：** /api/system/user/userSignUp
- **请求方法：** POST
- 请求参数：

| 参数名称        | 类型   | 是否必须 | 描述         |
| :-------------- | :----- | :------- | :----------- |
| username        | string | true     | 用户名       |
| password        | string | true     | 密码         |
| confirmPassword | string | true     | 确认密码     |
| firstName       | string | true     | 名字（必须） |
| lastName        | string | false    | 名字(可选)   |

- 返回结果：

| 参数名称   | 类型   | 是否必须 | 描述                                     |
| :--------- | :----- | :------- | :--------------------------------------- |
| token      | string | true     | 用户名                                   |
| userType   | int    | true     | 密码                                     |
| username   | string | true     | 确认密码                                 |
| firstName  | string | true     | 名字（必须）                             |
| lastName   | string | false    | 名字(可选)                               |
| userId     | int    | true     | 用户 id                                  |
| colorId    | int    | true     | 用户头像没有时显示颜色 id(0-17 随机生成) |
| avatar     | int    | false    | 用户头像 id, 没有头像返回 0              |
| avatarUrl  | string | false    | 用户头像地址, 没有头像返回空             |
| avatarName | string | false    | 用户头像名称, 没有头像返回空             |

```json
{
  "respCode": "10000",
  "respMsg": "operate success",
  "success": 1,
  "content": {
    "token": "token",
    "userType": "",
    "username": "",
    "firstName": "",
    "lastName": "",
    "userId": "",
    "colorId": "",
    "avatar": "头像id",
    "avatarUrl": "",
    "avatarName": ""
  }
}
```

## login

- **接口地址：** /api/system/userLogin/login
- **请求方法：** POST
- 请求参数：

| 参数名称 | 类型   | 是否必须 | 描述   |
| :------- | :----- | :------- | :----- |
| username | string | true     | 用户名 |
| password | string | true     | 密码   |

- 返回结果：

| 参数名称   | 类型   | 是否必须 | 描述                                     |
| :--------- | :----- | :------- | :--------------------------------------- |
| token      | string | true     | 用户名                                   |
| userType   | int    | true     | 密码                                     |
| username   | string | true     | 确认密码                                 |
| firstName  | string | true     | 名字（必须）                             |
| lastName   | string | false    | 名字(可选)                               |
| userId     | int    | true     | 用户 id                                  |
| colorId    | int    | true     | 用户头像没有时显示颜色 id(0-17 随机生成) |
| avatar     | int    | false    | 用户头像 id, 没有头像返回 0              |
| avatarUrl  | string | false    | 用户头像地址, 没有头像返回空             |
| avatarName | string | false    | 用户头像名称, 没有头像返回空             |

```json
{
  "respCode": "10000",
  "respMsg": "operate success",
  "success": 1,
  "content": {
    "token": "token",
    "userType": "",
    "username": "",
    "firstName": "",
    "lastName": "",
    "userId": "",
    "colorId": "",
    "avatar": "头像id",
    "avatarUrl": "",
    "avatarName": ""
  }
}
```


## logout

- 退出登录
- **接口地址：** /api/system/userLogin/logout
- **请求方法：** POST
- 请求参数：

| 参数名称 | 类型 | 是否必须 | 描述 |
| :------- | :--- | :------- | :--- |
