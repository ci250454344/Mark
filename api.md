## 渣男api接口
我们提供了一个 API 接口，可以通过接口获得指定数量和返回值格式的内容。接口的使用方式如下所示：
基本使用：
GET https://api.lovelive.tools/api/SweetNothings
使用此方法将会返回纯文本的一句随机的内容。
高级使用：
GET https://api.lovelive.tools/api/SweetNothings/:count/Serialization/:serializationType
GET https://api.lovelive.tools/api/SweetNothings/Serialization/:serializationType/:count
GET https://api.lovelive.tools/api/SweetNothings/Serialization/:serializationType
GET https://api.lovelive.tools/SweetNothings/:count
Url 变量说明：
serializationType：返回内容的格式，可以选择 Text 或 Json 格式。Text 格式会根据 count 的值以换行为分隔返回内容，Json 格式会在 returnObj中 包含返回一个 Array<string>。
count：要获取的数量。如果不在 Url 中使用这个参数 ，将默认获取 1 个句子。
Json 格式返回值的示例：
GET https://api.lovelive.tools/api/SweetNothings/3/Serialization/Json


```
 
    {
        code: 200,
        message: "",
        returnObj: [
            "她再也没有对我说过晚安，我的失眠也再没好过。",
            "从遇见你的那一天起，我所走的每一步都是为了更接近你。"
        ]
    }
    
```


## 成语接龙api

```

  http://i.itpk.cn/api.php?question=@cy[成语]

```
