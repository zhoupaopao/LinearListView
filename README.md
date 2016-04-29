# LinearListView
Android开源库：解决ScrollView与ListView的冲突解决方案
##适用场景
1、UI布局过长，屏幕无法全部显示，需要引入ScrollView来进行滚动，该lib自动兼容了屏幕过长而需要进行ScrollView嵌入的操作。
2、布局中一般的View和ListView需要混用的场景，Android原生不支持ScrollView与ListView混用，会导致ListView的measure异常，如果直接指定ListView高度，又会导致ListView的复用功能失效，容易OOM，该lib检测布局如果有ListView的话，会进行兼容性处理。
3、支持代码中动态设置ListView的显示状态，会实时根据ListView是否可见对布局兼容进行处理。
##使用方法
1、拷贝LinearListView.java文件到你项目的任何一个位置。
2、直接将LinearListView这个ViewGroup类进行在项目需要以上功能需求的位置嵌入即可。
3、详细方法参见demo。
```xml
<com.net168.view.LinearListView 
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    >
    <TextView
        android:layout_width="match_parent"
        android:layout_height="60dp"
        android:background="@color/red"
        android:text="@string/text_one"
        />
    <ListView
        android:id="@+id/listview"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        />
</com.net168.view.LinearListView>
```
