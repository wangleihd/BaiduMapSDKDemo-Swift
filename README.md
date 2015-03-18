# BaiduMapSDKDemo-Swift
使用百度地图 SDK创建的 DEMO，具体样式参考自官方 DEMO，使用 Swift 语言编写

##版本说明
1. 目前采用的是百度地图 iOS SDK 2.6.0
2. Xcode版本采用的是6.2
3. 项目采用 Swift 语言来进行编写
4. 项目采用 Storyboard 技术，试图以最简单的方式来展示百度地图 SDK 的使用

##功能说明

在使用前请定位到 `AppDelegate.swift`文件中，将 ak 更换为自己的百度地图 ak

应用界面如下图所示，主要提供了以下几种功能：

![主界面](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8A%E5%8D%8811.39.21.png)

###基本地图功能

能够显示基础地图，支持多点触摸、双击放大、多点单击缩小、旋转等手势操作，效果如图所示：

![基本地图功能](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8A%E5%8D%8811.39.29.png)

在地图加载完成后，会弹出一个提示框提示“MapView 已加载完成”。这个类主要完成最基本的地图界面的加载。

###多地图使用功能

![多地图使用功能](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8A%E5%8D%8811.39.36.png)

同时显示两个地图，一个是卫星图，一个是普通矢量图。

###图层展示功能

![图层展示功能](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8A%E5%8D%8811.39.43.png)

提供卫星图和矢量图的切换，同时可以打开路况开关、3D 楼宇开关以及百度自有热力图的开关。这里 UI 采用 StoryBoard 形式来实现，比较冗余。

###地图操作功能

![地图操作功能](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8A%E5%8D%8811.39.49.png)

提供缩放级别、旋转度、俯视度的精确定义和修改，同时实现点击、双击、长按手势的响应，自此之后采取代码添加 Map 的形式来实现，代码较为复杂，因为采取了手动添加约束。

此外，还提供了截图功能，可以将当前缩放级别的地图保存在系统自带的相册当中。

###UI 控制功能

![UI 控制功能](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8A%E5%8D%8811.39.54.png)

提供是否允许手势缩放、平移的控制，以及是否显示比例尺、设置指南针位置等设置，UI 同上。

###定位功能

**开启定位功能**

> 注意，采取模拟器来模拟定位功能时，请使用 Debug -> Location -> Custom Location来手动定义当前位置。如果没有显示，或者定位功能启动失败，请先选择 “无”或者“Apple”，然后再重新定义当前位置。

![定位功能开启](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.15.45.png)

定位功能开启后，是以普通态来显示的定位图标，也就是一个圆点。

**跟随态**

![跟随态](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.16.26.png)

跟随态是以一个箭头的方式来显示。

**罗盘态**

![罗盘态](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.16.21.png)

罗盘态是以一个罗盘的方式来显示的。

###覆盖物功能

**内置覆盖物**

![内置覆盖物](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.16.32.png)

内置覆盖物当中主要有虚线、矩形、线条、圆、多边形的自定义绘制。

**添加标注**

![添加标注](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.16.34.png)

添加标注主要添加一个可移动的标注以及一个不可移动的自动变化样式的自定义标注。

**图片图层**

![图片图层](https://github.com/SemperIdem/BaiduMapSDKDemo-Swift/blob/master/Screenshots/iOS%20Simulator%20Screen%20Shot%202015%E5%B9%B43%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.16.40.png)

图片图层主要是添加一个图片到地图视图上。

###POI 搜索功能

POI（Point of Interest），中文可以翻译为“兴趣点”。在地理信息系统中，一个POI可以是一栋房子、一个商铺、一个邮筒、一个公交站等。

本例子主要提供了一个简易的城市内检索例子，能够搜索某一个城市内的目标地点，一次显示10个，可以多次进行检索。

###地理编码功能

地理编码指的是将地址信息建立空间坐标关系的过程。又可分为正向地图编码和反向地图编码。
正向地理编码指的是由地址信息转换为坐标点的过程。
反向地理编码服务实现了将地球表面的地址坐标转换为标准地址的过程。反向地理编码提供了坐标定位引擎，帮助用户通过地面某个地物的坐标值来反向查询得到该地物所在的行政区划、所处街道、以及最匹配的标准地址信息。通过丰富的标准地址库中的数据，可帮助用户在进行移动端查询、商业分析、规划分析等领域创造无限价值。

###路径规划功能

提供了公交换乘、驾车和步行三种类型的线路规划方案。并且还可以查询驾车行驶中出现途经点的线路规划方案。

###公交线路查询

实现了查询某城市某路公交线路的查询功能，并且可以分别查询其上行路线和下行路线。

##-----------以下未完成--------------

###自定义绘制

###离线地图功能

###热力图功能

###短串分享功能

###云检索功能

###调起百度导航功能

###OpenGL 绘制功能

##待解决问题

1.iOS SDK 2.6.0 版本，Xcode 会提示一个警告：

> ld: warning: instance method 'update3DView:overlook:' in category from /Users/semper_idem/编程项目/BaiduMapTest/libs/Release-iphonesimulator/libbaidumapapi.a(BMKMapView.o) overrides method from class in /Users/semper_idem/编程项目/BaiduMapTest/libs/Release-iphonesimulator/libbaidumapapi.a(BMKAnnotationView.o)


大体意思是百度的 SDK 中的BMKMapView.o这个文件重写了BMKAnnotationView.p这个文件的update3DView:overlook:这个方法。因此会导致后面这个文件的这个方法不可用。

这个是 SDK 2.6.0的一个 BUG，目前官方尚未给出解决方法，只是提出没有任何影响，因为那个方法并不会被调用。

3.仅对 iPhone 5s 做了简要的适配，对 iPad 以及 iPhone 6 Plus 等设备的适配并未完善。
