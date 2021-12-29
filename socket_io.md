
# socket API

> 目前整理了部分文档


# pagination

param
```javascript
/*
    limit: int
    hash: bigint
    offsetId: int
    addOffset: int
    max_date: bigint
    min_date: bigint
   */
```
hash
```text
hash = 0
for id in ids:
    hash = (((hash * 0x4F25) & 0x7FFFFFFF) + id) & 0x7FFFFFFF
```



# 联系人模块 Working with contacts

### 增加联系人 contactAdd

>  Add an existing telegram user as contact.

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
userId: int,option
username: string,required
firstName: string,required
lastName： string,option
*/
```
Result
```javascript
/*
success: int
contact: object<contact>
user: object<user>
*/
```


### 删除联系人contactDelete

>  Deletes several contacts from the list.

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
id: array<int>,required
*/
```
Result
```javascript
/*
success: int
id: array<int>,
*/
```


### 编辑联系人信息 contactEdit

>  Edit contacts.

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
contact: object<contact>,required
*/
```
Result
```javascript
/*
success: int
contact: object<contact>,
*/
```


# 更新历史消息等等Working with updates

### messageUpdate

> updates: Object which is perceived by the client without
> a call on its part when an event occurs.

Result
```javascript
/*
type: string messageUpdate
success: int
updates: object<Update>
users 
chats
date
seq

*/
```

### messageUpdateDifference

> Get new updates.

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
pts: int
pts_total_limit: int
date: int
*/
```

Result
```javascript
/*
success: int
difference: array<>

*/
```



# 对话列表相关 Working with dialogs

### 获取对话列表 messageDialogsGet 

> Returns the current user dialog list.

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
limit: int
hash: bigint
offsetId: groupId
offsetDate： 对话改变时间
*/
```
Result
```javascript
/*
success: int
groupId: int
hash: int
limit: int
hash: bigint
offsetId: groupId
offsetDate： 对话改变时间

isEmpty: bool,
dialog: array<chat>
groupUser: array<groupUser>,
deleteGroupUser: array<int>,

*/
```

### 获取在线信息 messageOnlinesGet

> Get count of online users in a chat

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
groupId: int
groupType: int
contactId: int
*/
```

Result
```javascript
/*
success: int
groupId: int
groupType: int
contactId: int
onlines: int
lastSeen: string
isOnline: bool

*/
```

# 获取保存的gif Working with GIFs (actually MPEG4 GIFs)

### messageGifSavedGet

>  Get saved GIFs

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
hash: int
*/
```
Result
```javascript
/*
success: int
hash: int
gif: array<file>,
*/
```


### messageGifSave

>  Add GIF to saved gifs list

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
id: int（fileId）
unsave: bool(Whether to remove GIF from saved gifs list)
*/
```
Result
```javascript
/*
success: int
hash: int
id: int,
unsave: bool
*/
```

### messageGifSearch

>  Search for GIFs

param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
q: string（Text query）
offset: int
*/
```
Result
```javascript
/*
success: int
findGif: array<gif>
*/
```



# 历史消息相关 Working with messages

### 删除消息 messageHistoryDelete

>  Deletes communication history.
param
```javascript
/*
type: string,required
authtoken: string,required
tokenId: int,required
groupId: int
justClear: int（Just clear history for the current user, without actually removing messages for every chat user）
revoke: int (Whether to delete the message history for all chat participants)
maxId: int (Maximum ID of message to delete)
*/
```
Result
```javascript
/*
success: int
groupId: int
pts:int 
ptsCount:int 
*/
```
