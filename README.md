# citySelect
citySelect  easyui  省市县区 三级联动插件   jquery插件

## 最近在做一个外包项目，需要用到省市县区的联动插件   由于用得是easyui   找了一圈没有合适的，索性自己弄了个
## 插件的写法完全继承easyui的插件风格，当然下拉框用的是easyui的combobox
## 插件初始化只需给div(容器)加个citySelect类名就好，插件会自行初始化
## 注意，由于我这边需求只需要保存文字即可，所以需要城市区划编码的请自己扩展，具体请看源码，只需要补充一下区划编码就好
## 如果能节约您一分的时间，给个star吧

![](https://github.com/cdoer/citySelect/blob/master/citySelect.gif)

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>Basic ComboTree - jQuery EasyUI Demo</title>
	<link rel="stylesheet" type="text/css" href="./themes/default/easyui.css">
	<link rel="stylesheet" type="text/css" href="./themes/icon.css">
	<link rel="stylesheet" type="text/css" href="../demo.css">
	<script type="text/javascript" src="./jquery.min.js"></script>
	<script type="text/javascript" src="./jquery.easyui.min.js"></script>
	<script type="text/javascript" src="./citySelect.js"></script>
</head>
<body>
	<div class="citySelect" data-options="value:'山西省#大同市#广灵县'"></div>
	<button id="test">test</button>
	<script>
		$(function(){
			$("#test").click(function(){
				console.log($(".citySelect").citySelect("getText"));
			});
		})
	</script>
</body>
</html>
```

## 可配置的参数
```
var defaultOpts = {
        split:"#",
        value:"",
        province:{
            width:130
        },
        city:{
            width:100
        },
        area:{
            width:100
        }
    };
```

## 可调用的方法
* setValue
```
$(".citySelect").citySelect("setValue","广西省#桂林市#象山区");
```

* getValue
```
$(".citySelect").citySelect("getValue");   
返回
{
  province："广西省",
  city:"桂林市",
  area:"象山区"
}
```

* getText
```
$(".citySelect").citySelect("getText"); 
返回
广西省#桂林市#象山区
```




