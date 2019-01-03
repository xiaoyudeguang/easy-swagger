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

	@Override
	public Object doService(List<LogInfo> infos) {
		Console.log("日志", infos);
		return "我最棒！";
	}

	@Override
	public void addLogConfig(EasyList keys) {
		keys.add("db_log_handler");
	}
}
```
> 自定义的日志处理器需要继承easy-log提供的AbstractLogBrancher抽象类。需要实现两个方法：doService()方法是真正的接收并处理日志的方法；addLogConfig()方法中将自定义的日志处理器中的@Brancher注解中的key参数注册到easy-log中，这样就可以在doService()方法接收日志信息了。