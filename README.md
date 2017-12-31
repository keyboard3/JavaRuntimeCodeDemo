# JavaRuntimeCodeDemo
查看运行时 class 字节码

# 步骤
**给动态代理代码中打断点**
<br>
<img src="images/debug.png" width="350">

**在sa-jdi.jar里，还有一个图形化的工具 HSDB，也可以用来查看运行的的字节码**
<br>
>sudo java -classpath "$JAVA_HOME/lib/sa-jdi.jar" sun.jvm.hotspot.HSDB

<img src="images/hsdb1.png" width="350">

**找出执行进程的 id**
<br>
<img src="images/processid.png" width="350">

**弹出图形化界面附加进程**
<br>
<img src="images/hsdb2.png" width="350">

**查看内存中的 class**
<br>
<img src="images/hsdb3.png" width="350">

**查看内存中动态代理的 $Proxy0.class**
<br>
<img src="images/hsdb4.png" width="350">

**找其中UserService中的一个方法查看**
<br>
<img src="images/hsdb5.png" width="350">

**可以查看到方法中会去调用InvocationHandler.invoke()方法**
<br>
<img src="images/hsdb6.png" width="350">