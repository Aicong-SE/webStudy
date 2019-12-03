## JSON

### 	1.JSON介绍

​		JSON:JavaScript Object Notation

​		在ajax中，允许将 复杂格式的响应数据 构建成 JSON的格式再进行响应

### 	2.JSON表现

#### 		1.JSON表示单个对象

​			1.使用 {} 表示单个对象

​			2.在 {} 中使用 key:value 的形式来表示属性(数据)

​			3.Key必须要用 " " 引起来

​			4.value如果是字符串的话，也需要用" "引起来

```javascript
    var obj = {
            "name":"王老师",
            "age" : 30,
            "gender" : "Unknown"
    }
```

#### 		2.JSON表示一个数组

​			1.使用 [] 表示一个数组

​			2.数组中允许包含若干JSON对象 或 字符串

​				1.使用JSON数组表示若干字符串

```javascript
	var arr = ["王伟超","王夫人","王小超"];
```

​				2.使用JSON数组表示若干对象

```javascript
    var arr = [
        {
            "name":"王老师",
            "age":30,
            "gender":"男"
                            },
        {
            "name":"王夫人",
            "age":28,
            "gender":"男"
                            }
        ];
```

#### 	3.使用 jq 的 each()  迭代数组

​		回顾 JS中遍历数组

```javascript
	var a = [{"name":"guoxiaonao", "age": 18 }, {"name":"guoxiaonao2", "age": 22}];
	
	for (var i = 0 ; i < a.length ; i++ ){
		var obj = a[i];
		console.log('name is ' + obj.name);
		console.log('age is '+ obj.age);
	}
```

​		1.$arr.each();

​			$arr : jQuery中的数组

```javascript
        //语法：
        $arr.each(function(index,obj){
            index:遍历出来的元素的下标
            obj:遍历出来的元素
        });
```

​		2.$.each()

```javascript
        //语法：
        $.each(arr,function(index,obj){});
        arr : js 中的普通数组
```

#### 	4.后台处理JSON

​		在后台查询出数据再转换为JSON格式的字符串，再响应给前端

​		1.后台先获取数据

​			类型允许为：元组|列表|字典

​		2.在后台将数据转换为符合JSON格式的字符串

​		3.在后台将JSON格式的字符串进行响应

#### 	5.Python中的JSON处理

```python
    import json
    jsonStr = json.dumps(元组|列表|字典)
    return jsonStr
```

​	Django中的JSON处理

```python
#方法1 使用Django中提供的序列化类来完成QuerySet到JSON字符串的转换
from django.core import serializers
json_str = serializers.serialize('json',QuerySet)
return HttpResponse(json_str)

#方法2
d = {'a': 1}
return JsonResponse(d)

```

#### 	6.前端中的JSON处理

​	服务器端响应回来的数据是 String，需进行转换

```javascript
JSON对象=JSON.parse(JSON字符串)
```

