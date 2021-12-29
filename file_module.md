
#### 9 上传文件

- **接口地址：** /api/upload/uploadImg
- **请求方法：** POST
- 请求参数：

| 参数名称 | 类型   | 是否必须 | 描述   |
| :------- | :----- | :------- | :----- |
| file     | string | true     | 流文件 |

- 返回结果：

| 参数名称   | 类型   | 是否必须 | 描述                                |
| :--------- | :----- | :------- | :---------------------------------- |
| id         | int    | true     | 文件 id                             |
| originUrl  | string | true     | 上传文件的原始图片地址              |
| url        | string | true     | 上传文件的压缩图片地址（70 \* 70 ） |
| originName | string | true     | 上传图片文件名                      |
| fileName   | string | true     | 文件生成后文件名                    |

```json
{
  "respCode": "10000",
  "respMsg": "operate success",
  "success": 1,
  "content": {
    "id": 123,
    "originUrl": "http://dsfs.ml/xxx",
    "url": "http://dsfs.ml/xxx",
    "originName": "上传时的文件名.jpg",
    "fileName": "file_123123123.jpg"
  }
}
```