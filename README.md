# 一行代码实现Android引导界面

欢迎关注微信公众号、长期为您推荐优秀博文、开源项目、视频

![](http://oi5nqn6ce.bkt.clouddn.com/itheima/booster/code/qrcode.png)

* 下载当前项目拷贝PageFragment,PageFragmentAdapter,PageFrameLayout 到你的项目当中,如果需要动画拷贝DepthPageTransformer和ZoomOutPageTransformer通过这几个类一行代码实现引导界面

### 拷贝如下代码到XML布局中
~~~
    <包名.PageFrameLayout
        android:id="@+id/contentFrameLayout"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
        
~~~        
### 拷贝如下内容到JAVA代码中
~~~
 contentFrameLayout = (PageFrameLayout) findViewById(R.id.contentFrameLayout);
        // 设置资源文件和选中圆点
        contentFrameLayout.setUpViews(new int[]{
                R.layout.page_tab1,
                R.layout.page_tab2,
                R.layout.page_tab3,
                R.layout.page_tab4
        }, R.mipmap.banner_on, R.mipmap.banner_off);
        如需要动画添加如下代码
        contentFrameLayout.setDepthPageTransformer();
        或者
        contentFrameLayout.setZoomOutPageTransformer();
~~~
一句代码搞定！用得着的朋友点个赞吧~ 

![image](https://github.com/LuckSiege/AppWhenThePage/blob/master/image/4F460B52-74BC-4700-8DCE-C1AA866597DE.png)
![image](https://github.com/LuckSiege/AppWhenThePage/blob/master/image/A720A335-401B-4846-83DF-CF2D6CFC1584.png)
