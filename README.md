# 在移动设备上h5页面使用rem适配
有两个页面，两个页面都能work，有以下不同

对比一下，有几个不同点：

1. 第二个版本的html 刚开始是没有申明 mate viewport的，他是页面渲染的时候，js后面动态加上去的

而且是根据不同的屏幕分辨率，手动调整的，下面是3倍分辨率上第二个版本的 meta viewport （iphone 6 plus）

所以如果是同一张图片的话，比如在iphone 6 plus （3倍分辨率上），这时候图片就会显得模糊（要解决这个方法就是要根据不同的分辨率引入不同的图片，html会有属性 data-dpr 来判断）


2. 第二个版本有手动引入一个js来计算viewport的属性

3. 对rem的引用，第二个版本会应用的比较彻底，除了会根据两个不同分辨率的大屏幕做统一适配之外，其他全部是用rem来计算，而对于不同屏幕的表现来看，第二个版本也会显得比较自然。
第一个版本虽然在屏幕适配上也没有问题，但是总的来说没有第二个版本自然。而且第一个版本的媒体查询的适配也会比较多一些，不过第一个版本还可以再优化。


总的来说，第二个版本会比较好，但是第二个版本要注意一点的是，对图片的处理，要根据不同的屏幕分辨率进行处理，比如如果是二倍屏，就要用二倍的图片。
