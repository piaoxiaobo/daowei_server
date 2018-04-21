# 接口文档
作者：卞荣成 <br>
网站：[小泊随記](https://www.itsolotime.com)<br>
博客：[漂小泊的博客](https://www.itsolotime.com/blog)<br>
GitHub地址：https://github.com/piaoxiaobo/daowei_server<br>
感谢[周振华]()的技术支持。
## 目录：
[1、获取主页服务数据](##获取主页服务数据)<br/>
[2、获取服务商数据](#获取服务商数据)<br/>
[3、获取评价数据](#获取评价数据)<br/>
[4、获取商家描述数据](#获取商家描述数据)<br/>
[5、请求示例](#请求示例)<br/>
[6、添加结构示例](#添加结构示例)<br/>



## 1、获取主页服务数据

### 请求URL：
	http://localhost:3000/service

### 请求方式：
	GET

### 参数类型：
	无

### 返回示例：
```
	{
	  "serve1": [
	    {
	      "imgUrl":"http://img.daoway.cn/img/price/2017/10/27/00d41623-8217-41e0-b299-7375d42d2cd0_thumb.jpg",
	      "name":"全身中式按摩套餐",
	      "price":288,
	      "description":"服务时长：70分钟 服务姿势：俯卧、仰卧 功效介绍：疏通经..."
    	}
	}

```
## 2、获取服务商数据

### 请求URL：
	http://localhost:3000/servicepro

### 请求方式：
	GET

### 参数类型：
	无
	
### 返回示例：

	{
	  "servicepro": [
	    {
	      "imgUrl":"http://img.daoway.cn/img/2016/12/28/5cf8680f-0264-4686-ba05-145700db6063_thumb.jpg",
	      "iconUrl":"https://www.itsolotime.com/img/home1.png",
	      "name":"云家政",
	      "estimate":86,
	      "order":47702
    		}
	}


## 3、获取评价数据

### 请求URL：
	http://localhost:3000/comment

### 请求方式：
	GET

### 参数类型：
	无

### 返回示例：
```
	{
	  "comment":[
	    {
	      "iconUrl":"http://img.daoway.cn/img/2017/12/30/adf81789-db5b-47d6-a0fb-efbdadc95b54.jpg",
	      "area":"普陀区",
	      "city":"上海",
	      "comment":"阿姨服务非常好，收拾的很干净。",
	      "createtime":1521196598000,
	      "nick":"啦啦6666",
	      "star":5
	    },
	}
```

## 4、获取商家描述数据

### 请求URL：
	http://localhost:3000/detail

### 请求方式：
	GET

### 参数类型：
	无

### 返回示例：
```
	{
	  "imgUrl":"http://img.daoway.cn/img/price/2017/12/06/47bb440b-5292-4100-8b16-88779f759bf5.jpg",
	  "name":"家庭保洁",
	  "price":35,
	  "oldPrice":45,
	  "soldCount":59700,
	}

```


## 5、请求示例
```
 $.ajax({
    type:"请求方式",
    url:"数据地址",
    dataType:"json",
    success:function(data) {
        console.log(data)
    },
    error:function(data){
        alert("您请求数据失败了，请检查您的请求方式以及地址！");
    }
});
```
## 6、添加结构示例
```
"<li class='test'><img src="+data.servicepro[i].imgUrl+" ><p>"+data.servicepro[i].name+"</p><span>"+data.servicepro[i].order+"</span></li>"
```
## 使用说明
1、启动服务器，查看服务器状态启动是否成功
2、在页面发送ajax请求，根据API获取后台数据
3、将获取数据添加至页面
4、添加页面结构可以自行设计，本demo结构示例仅供参考


**注意：服务商数据为重复信息，陆续进行更新。本服务器为测试版本，不代表最终版本。**