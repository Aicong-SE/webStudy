# ajax-jquery 

#### 1.$obj.load()

​		作用：载入远程的HTML文件到指定的元素中

```javascript
$obj.load(url,data,callback)
	$obj:显示响应内容的jq元素
	url:请求地址
	data:请求参数(可省略)
		方式1:字符串传参
		"key1=value1&key2=value2"
		注：此种传参会使用 get 方式发送请求
		方式2:使用JS对象传参
		{
   		 key1:"value1",
         key2:"value2"
		}
		注：此种传参会使用 post 方式发送请求
	   callback:响应成功后的回调函数(可省略)

```

#### 2.$.get() 和 $.post()

​		作用：通过get方式异步的向远程地址发送请求

```javascript
$.get(url,data,callback,type)
		url:请求地址
		data:传递到服务器端的参数
		可以是字符串 ："name=sf.zh&age=18"
		也可以是js对象:
			{
				name:"sf.zh",
				age:18
			}
		callback:响应成功后的回调函数
        ex: function(data){
           console.log(data)
        }
		type:响应回来的数据的格式
			取值如下:
			1.html : 响应回来 的文本是html文本
			2.text : 响应回来的文本是text文本
			3.script : 响应回来的文本是js执行脚本
			4.json : 响应回来的文本是json格式的文本
```

#### 3. $.ajax()

```javascript
参数对象中的属性：
	1.url : 字符串，表示异步请求的地址
	2.type : 字符串，请求方式，get 或 post
	3.data : 传递到服务器端的参数
		可以是字符串 ："name=sf.zh&age=18"
		也可以是js对象:
			{
				name:"sf.zh",
				age:18
			}
	4.dataType : 字符串，响应回来的数据的格式
		1.'html'
		2.'xml'
		3.'text' 
		4.'script'
		5.'json'
		6.'jsonp' : 有关跨域的响应格式
	5.success:回调函数，请求和响应成功时回来执行的操作
	6.error : 回调函数，请求或响应失败时回来执行的操作
	7.beforeSend : 回调函数，发送ajax请求之前执行的操作，如果return false，则终止请求
```

