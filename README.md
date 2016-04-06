# Dagger2
Dagger2学习笔记
只调用DaggerxxxComponent.create().inject(mContainer)的时候就会初始化被@inject标记的xxx的实例。
如果Module只有有参构造器，则必须显式传入Module实例。
一个Component可以包含多个Module，这样Component获取依赖时候会自动从多个Module中查找获取，Module间不能有重复方法。添加多个Module有两种方法，一种是在Component的注解@Component(modules={××××，×××}) 添加多个modules
另外一种添加多个Module的方法可以被使用Module中的@Module（includes={××××，×××}）

Component定义方法的规则

1）对应上面苹果容器的例子，Component的方法输入参数一般只有一个，对应了需要注入的Container。有输入参数返回值类型就是void 
2）Component的方法可以没有输入参数，但是就必须有返回值
