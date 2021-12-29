#### mergeUsername

- 修改 username
- **接口地址：** /api/account/person/mergeUsername
- **请求方法：** POST
- 请求参数：

| 参数名称 | 类型   | 是否必须 | 描述   |
| :------- | :----- | :------- | :----- |
| username | string | true     | 用户名 |

- 返回结果：

| 参数名称 | 类型 | 是否必须 | 描述 |
| :------- | :--- | :------- | :--- |


```json
{
  "respCode": "10000",
  "respMsg": "operate success",
  "success": 1,
  "content": {}
}
```


#### mergeName


- 修改 firstName 和 lastName
- **接口地址：** /api/account/person/mergeName
- **请求方法：** POST
- 请求参数：

| 参数名称  | 类型   | 是否必须 | 描述         |
| :-------- | :----- | :------- | :----------- |
| firstName | string | true     | 名字         |
| lastName  | string | false    | 名字（可选） |

- 返回结果：

| 参数名称 | 类型 | 是否必须 | 描述 |
| :------- | :--- | :------- | :--- |


```json
{
  "respCode": "10000",
  "respMsg": "operate success",
  "success": 1,
  "content": {}
}
```

#### mergeAvatar


- 修改头像
- **接口地址：** /api/account/person/mergeAvatar
- **请求方法：** POST
- 请求参数：

| 参数名称 | 类型 | 是否必须 | 描述    |
| :------- | :--- | :------- | :------ |
| avatar   | int  | true     | 头像 id |

- 返回结果：

| 参数名称 | 类型 | 是否必须 | 描述 |
| :------- | :--- | :------- | :--- |


```json
{
  "respCode": "10000",
  "respMsg": "operate success",
  "success": 1,
  "content": {}
}
```

#### mergeEntity

- 8 一次性修改所有个人信息
- **接口地址：** /api/account/person/mergeEntity
- **请求方法：** POST
- 请求参数：

| 参数名称 | 类型 | 是否必须 | 描述 |
| :------- | :--- | :------- | :--- |


| avatar | int | false | 头像 id |
| email | string | false | 邮箱 |
| address | string | false | 地址 |
| password | string | false | 新的密码 |
| oldPassword | string | false | 旧的密码 |

- 返回结果：

| 参数名称 | 类型 | 是否必须 | 描述 |
| :------- | :--- | :------- | :--- |


```json
{
  "respCode": "10000",
  "respMsg": "operate success",
  "success": 1,
  "content": {}
}
```
