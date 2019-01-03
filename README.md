# easy-swagger

## 介绍
当你出于不想写文档的目的使用swagger的时候，有没有觉得，其实，工作量一点都没少？该写的一点没少，之前是写文档，现在是写一堆注解，是不是心里一万句草泥马策马奔腾。现在，easy-swagger来了，简化你的sawgger使用体验，从此，踏上人生巅峰！github项目地址：https://github.com/xiaoyudeguang/easy-swagger

## 使用说明

## Maven引用(如果版本有变化，请自行去maven中央仓库引用)
```
<dependency>
    <groupId>io.github.xiaoyudeguang</groupId>
    <artifactId>easy-swagger</artifactId>
    <version>3.0.4-RELEASE</version>
</dependency>
```

## 使用案例
```
@SpringController( value= “democontroller", todo = { “easy-swagger使用示例" })
public class DemoController{

	@SpringMapping( value= “test", todo = { “easy-swagger示例方法" })
	public Object test(string name, string age) {
		Console.log( name, age);
		return “easy-swagger is an good tool！";
	}
}
```

## swagger管理效果

到这里，你就可以骄傲的打开浏览器查看效果了(地址自己找去，网上很多。关于swagger的管理页面界面，码云或者其他地方一找一大堆，不同的插件有不同的访问地址，酌情自己修改访问地址即可)。就问你简单不？那啥，好用你就持续关注吧！

PS：easy-swagger已经替你完成了swagger的配置，请不要再配置一遍了。只需要把你喜欢的插件引入你的项目，访问插件提供的访问地址即可。

