Android studio项目导入build.gradle文件不是导入文件夹

view的setSelected()方法设定布尔值设置控件是否被选中，在控件的background中设置@drawable/xxxx（xml文件）  更改控件是否选择时的颜色
style目录下的color文件定义用到的颜色，比在layout下定义好。

private static final String TAG = “xxx”  用于logcat调试输出

https://www.jianshu.com/p/9f22911ea630   串口工具文档

https://www.runoob.com/  菜鸟教程：各语言中文api

dmrfcoder *github用户       F1ReKing  *Android-SerialPort串口调试库开发者

switch中break和return的区别，break是退出一层，return退出函数

多个RadioButton不用RadioGroup实现单选  先监听点击事件，写setRadioButtonCheck(v.getId())类，使用SparseArray数组。实现单选，看微信收藏笔记radiobutton

implementation 'me.jessyan:autosize:1.1.2' 屏幕适配（AndroidAutoSize）

获取ViewGroup------MainActivity activity;                               
返回View:       activity.getWindow().getDecorView()                  
返回ViewGroup： (ViewGroup)activity.getWindow().getDecorView()

2018 I/O大会Google强推androidx彻底弃用了Android.support.V7/V4  不过只有软件包和 Maven 工件名称发生了变化；类、方法和字段名称没有改变。

弹出式菜单 PopupMenu    弹出式窗口 PopupWindow  Toolbar可以自定义导航栏

（1）onCreate:create表示创建，这是Activity生命周期的第一个方法，也是我们在android开发中接触的最多的生命周期方法。它本身的作用是进行Activity的一些初始化工作，比如使用setContentView加载布局，对一些控件和变量进行初始化等。但也有很多人将很多与初始化无关的代码放在这，其实这是不规范的。此时Activity还在后台，不可见。所以动画不应该在这里初始化，因为看不到
（2）onStart:start表示启动，这是Activity生命周期的第二个方法。此时Activity已经可见了，但是还没出现在前台，我们还看不到，无法与Activity交互。其实将Activity的初始化工作放在这也没有什么问题，放在onCreate中是由于官方推荐的以及我们开发的习惯。
（3）onResume:resume表示继续、重新开始，这名字和它的职责也相同。此时Activity经过前两个阶段的初始化已经蓄势待发。Activity在这个阶段已经出现在前台并且可见了。这个阶段可以打开独占设备
（4）onPause:pause表示暂停，当Activity要跳到另一个Activity或应用正常退出时都会执行这个方法。此时Activity在前台并可见，我们可以进行一些轻量级的存储数据和去初始化的工作，不能太耗时，因为在跳转Activity时只有当一个Activity执行完了onPause方法后另一个Activity才会启动，而且android中指定如果onPause在500ms即0.5秒内没有执行完毕的话就会强制关闭Activity。从生命周期图中发现可以在这快速重启，但这种情况其实很罕见，比如用户切到下一个Activity的途中按back键快速得切回来。
（5）onStop：stop表示停止，此时Activity已经不可见了，但是Activity对象还在内存中，没有被销毁。这个阶段的主要工作也是做一些资源的回收工作。
（6）onDestroy：destroy表示毁灭，这个阶段Activity被销毁，不可见，我们可以又将还没释放的资源释放，以及进行一些回收工作。
（7）onRestart：restart表示重新开始，Activity在这时可见，当用户按Home键切换到桌面后切回来或者从后一个Activity切回前一个Activity就会触发这个方法。这里一般不做什么操作。

Java与数据库中的datetime Timestamp以及String之间的转换https://blog.csdn.net/weixin_43959046/article/details/90322346

Android studio满屏报错Duplicate class com.google.zxing.BarcodeFormat found in modules jetified-core-3.4.0.jar      这是应为重复导入jar包导致的，把implementation改为compileOnly就好了（改的是父包，不是重写/继承父包的那个包）

notes有配置as文件目录的方法，减少c盘占用。

Navigation  导航

简书：   https://www.jianshu.com/p/f4b5b1010a41
ldpi：240x320
mdpi：320x480
hdpi：480x800、480x854
xhdpi：至少960*720  720p
xxhdpi：1920×1080  1080p

xutils3绑定控件，控件监听，绑定函数....只能使用private！！！使用其它修饰符不起作用。

startActivity(new Intent(Settings.ACTION_BLUETOOTH_SETTINGS)); //打开蓝牙系统设置界面
startActivity(new Intent(Settings.ACTION_WIFI_SETTINGS)); //打开wifi网络系统设置界面
startActivity(new Intent(Settings.ACTION_DATE_SETTINGS));//打开时间系统设置界面

&& b：a和b同时为true 才返回 true， 否则返回false；            a || b：a或b任意一个为true 就返回true ， 否则返回false     判断多个输入框不为空要用||，只要有一个为空就是true，回进入if语句，用&&会导致有一个不是空，返回false，进不去if。或者把所有的&&框起来进行取反   ！
