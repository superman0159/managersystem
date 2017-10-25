# 自动响应
## `/command`为父级目录：

### 查询全部指令
#### URL

#####`GET:` `/query/`

#### INPUT

```json
	null
```

#### OUTPUT

```JSON
//json数组
	[
    {
        "contentList":[     		//内容集合
            {
                "commandId":"2", 	//指令ID
                "content":"2",		//内容
                "id":"2",			//内容ID
                "url":"2"			//链接
            }
        ],
        "description":"今日新闻",		//指令描述
        "id":"2",					//指令ID
        "name":"新闻"				//指令名称
    },
    {
        "contentList":[
            {
                "commandId":"3",
                "content":"3",
                "id":"3",
                "url":"3"
            }
        ],
        "description":"精选段子",
        "id":"3",
        "name":"段子"
    }
]

```

#### ERROR
* `timeout` 

----
### 根据ID查询指令
#### URL

#####`GET:` `/query/{id}/`

#### INPUT

```json
	id  //数值
```

#### OUTPUT

```JSON
//json对象
    {
        "contentList":[     		//内容集合
            {
                "commandId":"2", 	//指令ID
                "content":"2",		//内容
                "id":"2",			//内容ID
                "url":"2"			//链接
            }
        ],
        "description":"今日新闻",		//指令描述
        "id":"2",					//指令ID
        "name":"新闻"				//指令名称
    }

```

#### ERROR
* `timeout` 

----
### 根据描述查询指令
#### URL

#####`GET:` `/query/{des}/`

#### INPUT

```json
	des //字符串
```

#### OUTPUT

```JSON
//json数组
[
    {
        "contentList":[     		//内容集合
            {
                "commandId":"2", 	//指令ID
                "content":"2",		//内容
                "id":"2",			//内容ID
                "url":"2"			//链接
            }
        ],
        "description":"今日新闻",		//指令描述
        "id":"2",					//指令ID
        "name":"新闻"				//指令名称
    },
    {
        "contentList":[
            {
                "commandId":"3",
                "content":"3",
                "id":"3",
                "url":"3"
            }
        ],
        "description":"精选段子",
        "id":"3",
        "name":"段子"
    }
]
```

#### ERROR
* `timeout` 

----
### 根据名称查询指令
#### URL

#####`GET:` `/query/{name}/`

#### INPUT

```json
	name  //字符串
```

#### OUTPUT

```JSON
//json数组
[
    {
        "contentList":[     		//内容集合
            {
                "commandId":"2", 	//指令ID
                "content":"2",		//内容
                "id":"2",			//内容ID
                "url":"2"			//链接
            }
        ],
        "description":"今日新闻",		//指令描述
        "id":"2",					//指令ID
        "name":"新闻"				//指令名称
    }
]
```

#### ERROR
* `timeout` 

----
### 插入指令及内容
#### URL

##### `POST:` `/insert/{id}/`

#### INPUT

```json 
{
        "contentList":[             //内容集合
            {
                "commandId":"2",    //指令ID
                "content":"2",      //内容
                "id":"2",           //内容ID
                "url":"2"           //链接
            }
        ],
        "description":"今日新闻",       //指令描述
        "id":"2",                   //指令ID
        "name":"新闻"             //指令名称
    }
```

#### OUTPUT

```JSON
	1 //插入成功
```

#### ERROR
* `timeout` 

----
### 根据ID删除指令
#### URL

##### `DELETE:` `/delete/command/{id}/`

#### INPUT

```json 
	id
```

#### OUTPUT

```JSON
	大于 1 //删除成功
```

#### ERROR
* `timeout` 

----
### 根据ID删除内容
#### URL

##### `DELETE:` `/delete/content/{id}/`

#### INPUT

```json 
	id
```

#### OUTPUT

```JSON
	大于 1 //删除成功
```

#### ERROR
* `timeout` 