# Dagger2
Dagger2学习笔记
只调用DaggerxxxComponent.create().inject(mContainer)的时候就会初始化被@inject标记的xxx的实例。
如果Module只有有参构造器，则必须显式传入Module实例。
一个Component可以包含多个Module，这样Component获取依赖时候会自动从多个Module中查找获取，Module间不能有重复方法。添加多个Module有两种方法，一种是在Component的注解@Component(modules={××××，×××}) 添加多个modules
另外一种添加多个Module的方法可以被使用Module中的@Module（includes={××××，×××}）
