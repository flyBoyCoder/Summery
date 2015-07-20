# Summery
1:导航条返回键带的title太讨厌了,怎么让它消失!
[[UIBarButtonItem appearance] setBackButtonTitlePositionAdjustment:UIOffsetMake(0, -60)
                                                      forBarMetrics:UIBarMetricsDefault];
2:怎么像safari一样滑动的时候隐藏navigationbar?
navigationController.hidesBarsOnSwipe = Yes

3:怎么播放GIF的时候这么卡，有没有好点的库？
FlipBoard出品的太适合你了：https://github.com/Flipboard/FLAnimatedImage

4:怎么把tableview里cell的小对勾的颜色改成别的颜色？
_mTableView.tintColor = [UIColor redColor];

5:本来我的statusbar是lightcontent的，结果用UIImagePickerController会导致我的statusbar的样式变成黑色，怎么办？
- (void)navigationController:(UINavigationController *)navigationController willShowViewController:(UIViewController *)viewController animated:(BOOL)animated
{
    [[UIApplication sharedApplication] setStatusBarStyle:UIStatusBarStyleLightContent];
}

6:怎么把我的navigationbar弄成透明的而不是带模糊的效果？
[self.navigationBar setBackgroundImage:[UIImage new]
                         forBarMetrics:UIBarMetricsDefault];
self.navigationBar.shadowImage = [UIImage new];
self.navigationBar.translucent = YES;

7:怎么改变uitextfield placeholder的颜色和位置？
继承uitextfield，重写这个方法
- (void) drawPlaceholderInRect:(CGRect)rect {
    [[UIColor blueColor] setFill];
    [self.placeholder drawInRect:rect withFont:self.font lineBreakMode:UILineBreakModeTailTruncation alignment:self.textAlignment];
}

8:tableviewCell 只显示高亮状态 不设置选中状态，只要重写
- (void)setSelected:(BOOL)selected animated:(BOOL)animated{
}

9:当设置navigationBar的背景图片时移除黑线的方法,该方法会使translucent属性失效
-(void)useShadowImageRemoveBlackLine
{
    //通过设置shadowImage移除黑线
    [self.navigationController.navigationBar setShadowImage:[UIImage new]];
}


#pragma mark 
1: 让编译器闭嘴的告警
   http://blog.csdn.net/mamong/article/details/24542107
2: ios工程如何支持64位
   http://www.cocoachina.com/cms/wap.php?action=article&id=10031

// 资料
1: http://gold.xitu.io/entry/558e563de4b060308e44daf9
2: http://blog.sina.com.cn/s/blog_71715bf801019oy8.html  操作手机通讯录
3: http://www.jianshu.com/p/7d4710b815c2       iOS 苹果官方Demo合集

// 博客
1 http://www.coderyi.com/
2 http://www.joyios.com
3 http://kittenyang.com/#blog  动画类 杨骑滔
4 http://southpeak.github.io/blog/ 南峰子老驴 含金量啊
5 http://zhangbuhuai.com/ 张不坏
6 http://www.cnblogs.com/   Kenshin Cui's Blog
7 http://www.hmttommy.com/
8 http://lcepy.github.io/archives/


// github
1: ios_top_1000
   https://github.com/iamdaiyuan/ios_top_1000
   https://github.com/vsouza/awesome-ios
2: blog
   https://github.com/tangqiaoboy/iOSBlogCN

// github东东
1: https://github.com/romaonthego
2：https://github.com/liufan321 刀哥
3：https://github.com/Yalantis 个个精品
4: https://github.com/jessesquires
5: https://github.com/sxyx2008/DevArticles/issues/91 主流动画
6: https://github.com/nsdictionary 

// 简书
1: http://www.jianshu.com/users/8d704c0faf00/latest_articles

// Swift资料
1: https://github.com/ipader/SwiftGuide
2: http://www.devtalking.com/
3: Swift 开源项目精选
https://github.com/ipader/SwiftGuide/blob/master/Featured.md


// 前端
http://dev.benbun.com/web/doc/
JSON格式化工具
http://www.runoob.com/tool/json/index.html

// CoreData
http://www.jianshu.com/p/3d703ec37d0b?utm_campaign=maleskine&utm_content=note&utm_medium=writer_share&utm_source=weibo



Swift
1: 元组
http://www.devtalking.com/articles/tuple-in-swift/
2: Optional
http://joeyio.com/ios/2014/06/04/swift---/
3: 泛型
http://zhangbuhuai.com/2015/05/14/Swift-Generics/
4: 函数
http://www.cnblogs.com/gcb999/p/3794625.html
5: 将 struct enum  的方法声明为 mutating 便于修改struct 或者 enum 内部的变量
http://swifter.tips/protocol-mutation/
6: typealias 和泛型接口
http://swifter.tips/typealias/






在Swift项目中使用OC，在OC项目中使用Swift
http://kittenyang.com/swiftandoc/
http://blog.kingiol.com/blog/2014/06/04/interactive-between-objective-c-and-swift/


在Swift项目中使用CocoaPods
platform :ios, '8.0'
source 'https://github.com/CocoaPods/Specs.git'
pod 'AFNetworking'
pod 'EGOTableViewPullRefresh'
pod 'SVProgressHUD'
pod 'FMDB'
