## iOS 多线程

- **pthread**

```
01 特点：
（1）一套通用的多线程API
（2）适用于Unix\Linux\Windows等系统
（3）跨平台\可移植
（4）使用难度大

02 使用语言：c语言
03 使用频率：几乎不用
04 线程生命周期：由程序员进行管理
```

- **NSThread**

是pthread的一个简单封装，偏向于底层，每个NSThread对象就是一个线程。基于线程使用。

```
01 特点：
（1）使用更加面向对象
（2）简单易用，可直接操作线程对象

02 使用语言：OC语言
03 使用频率：偶尔使用
04 线程生命周期：由程序员进行管理
```

- **GCD**

是基于C的API，基于task使用。 有并行队列和串行队列，并行队列将多个任务分配到不同线程。

```
01 特点：
（1）旨在替代NSThread等线程技术
（2）充分利用设备的多核(自动)

02 使用语言：
03 使用频率：经常使用
04 线程生命周期：自动管理
```

- **NSOperation & NSOperationQueue**

是基于GCD封装的NSObject对象，基于队列使用。

```
01 特点：
（1）基于GCD（底层是GCD）
（2）比GCD多了一些更简单实用的功能
（3）使用更加面向对象

02 使用语言：OC语言
03 使用频率：经常使用
04 线程生命周期：自动管理
```


### 参考

- [GCD 深入理解（一）](http://www.cocoachina.com/industry/20140428/8248.html)
- [GCD 深入理解（二）](http://www.cocoachina.com/ios/20140515/8433.html)
- [iOS多线程与GCD 你看我就够了](http://www.cocoachina.com/ios/20160804/17291.html)
- [关于iOS多线程，你看我就够了（已更新）](http://www.cocoachina.com/ios/20150731/12819.html)