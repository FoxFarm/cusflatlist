# 欢迎使用 cusflatlist

------

这个是一个基于React-Native的封装的flatlist,建议使用RN >=0.48以上版本 自动带有上拉加载和下拉刷新 。
下载安装： npm install cusflatlist
如何使用： 
> * 建议在使用封装一层

> * 导入方法体：  loadApi(page = 1, postRefresh, error) {  let {list = []} = fetch(); postRefresh(list, pageLimit, pageSize);  if (false) {  error(); }  }
> * 如何调用这个库： 
```python
import {NewList} from "cusflatlist"
 <NewList
{...this.props}//不能少
method={this.loadApi}
renderItem={this.renderItem} // 返回(item, index)
/>
```
API 说明

 | api   |调用 |属性  |
 | --------   | -----:  | :----:  |
| 效果调用  refreshableMode模式      | 默认安卓：android_base   |  默认ios：ios_base  |
| renderItem子类item     | renderItem = {it}一样的自定义一个it，然后在我们的it就可以使用使用this.props.item调用数据和this.props.index调用第几个 |   item，index    |
| 在renderItem里面调用点击事件以及跳转        |  直接this.props.navigation.navigate()配合react-navigation或者react-navite-navigation这些一样的  |
| ListEmptyComponent空白页面设置        |   导入页面ListEmptyComponent = {enmptyview}//空白页面 enmptyview是导入的控件外部 |
|ListHeaderComponent头部定义  |和空白页面设置一样 |
| numColumns   |设置列数 #horizontal |设置横向和纵向（true和false）  |


