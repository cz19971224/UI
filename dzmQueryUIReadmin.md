# dzmQueryUI 全局样式说明文档
## 清空默认样式

## 布局
.dzm-container    设置为容器：水平方向居中  宽度为100% 高度没有
.dzm-container-fluid  宽度为100%的容器  没有外边距 内边距左右15px
上下0px 没高度


## 按钮  mm-btn
成功  mm-btn-success 
警告  mm-btn-warning
错误  mm-btn-error
取消  mm-btn-cancel
确认  mm-btn-sure
默认  mm-btn-default
危险  mm-btn-danger
首选  mm-btn- primary
一般信息   mm-btn-info
禁止按钮   mm-btn-disable
百搭按钮   mm-btn-normal
暖色按钮   mm-btn-warm


#### 渐变的按钮样式
成功  mm-btn-success-rgb
警告  mm-btn-warning-rgb
错误  mm-btn-error-rgb
取消  mm-btn-cancel-rgb
确认  mm-btn-sure-rgb
默认  mm-btn-default-rgb
危险  mm-btn-danger-rgb
首选  mm-btn- primary-rgb
一般信息   mm-btn-info-rgb
禁止按钮   mm-btn-disable-rgb
百搭按钮   mm-btn-normal-rgb
暖色按钮   mm-btn-warm-rgb

#### 伪类按钮样式
成功  mm-btn-success-hover
警告  mm-btn-warning-hover
默认  mm-btn-default-hover
危险  mm-btn-danger-hover



-型号
大   mm-btn-bg
小   mm-btn-sm
中   mm-btn-md

-圆角按钮  mm-btn-radius


## 表单

## 滑块

## select选择框

## 表格 .table
.table 表示基础表格；必须在table标签中使用；表示只有列边框的表格
.table-striped 表示条状表格；表体的偶数行；有一定的背景颜色
.table-column 表示半边框样式
.table-condensed  表示紧凑表格
.table-border  边框表格
.table-inverse  背景色为黑色的表格
.table-inverse-striped 黑色条形表格 
.table-inverse-hover  黑色悬浮样式  需要依赖 .table-inverse 或者.table-inverse-striped 黑色条形表格
.table-control 表示【控制页】 固定；其他列可以滚动  .table-control必须给table标签的祖籍元素添加；而不是给父元素添加 .table-box表示table的父容器
~~~css
.table-control{
    position:relative;
}
.table-control table>tr>td:last-child{
    position:absolute;
    right:0;
    min-width:120px;
    text-align:center;
    box-shadow:-5px 4px 6px 1px #ccc;
}
/* 选中倒数第二列：解决内容遮罩问题 */
.table-control table>tr>td:nth-last-child(2)::before{
    content:'';
    width:120px;
}
.table-control>.table-box{
    overflow:auto
}
~~~~


移动端
.table-responsive 移动端表格: 可以有横向滚动的效果  .table-responsive 需要给table 的父容器添加

状态表格  给tr 添加类名 
.success  成功
.info     通用
.warning   警告
.danger   危险
.primary  首选 
.warm     暖色


## 栅格系统




## 分页 .page
.pagination  实现分页样式  有 ul li a 完成的分页效果
.pagination-bgc  表示有背景颜色的分页
.pagination-inverse  黑色的分页 #393d49

## 表单类

###单选多选框样式
.circle-check 圆形选择框    .circle-checbo 需要给input[type=checkbox]的父元素添加
.suqare-check 正方形选择框  .square-checbo 需要给input[type=checkbox]的父元素添加
/* 示例代码 */
<div class="circle-check">
        <input type="checkbox">
    </div>
    <div class="square-check">
        <input type="checkbox">
    </div>
~~

###滑块 .sliderbar
.slider-wrap表示进度条外围容器
.sliderbar 表示滑块的条
.sliderbar-control 表示控制键
~~~html
 <div class="slider-wrap">
        <div class="sliderbar">
            <div class="sliderbar-control">
                55
            </div>
        </div>
    </div>
~~~
状态
.sliderbar-success
.sliderbar-info
.sliderbar-primary
.sliderbar-error

### 开关 .switch
.switch 开关样式的选择框  需要给 input[type=checkbox] class=switch 才能实现效果
   -绿色我开 input=checked 灰色为关 input=disable
状态
.switch-info 蓝色开 灰关
.switch-danger 红开 灰关
.switch-warm 橙开 灰关
.switch-primary 蓝开 红关


### 步骤组件 step
.step-wrap 为外部容器 55rem
.step-full 每个步骤容器  包含内容 :圈 线 文本
.step-line-box 具体进行的每一步 用Input[type=checkbox],当有checked属性 表示当前步骤已经完成
.step-circle 表示 圈
.step-line 表示 线
.step-text 表示步骤内容

状态
.step-circle-info
.step-circle-success
.step-circle-primary
.step-circle-warm
.step-circle-error
.step-circle-danger

### 导航  .nav
注意：导航仅仅适用于pc端应用；且只使用与静态的样式 导航中所有的样式都是操作li下a标签
.nav-tab 表示tab样式的导航条  需要依赖.nav
.nav-pills 胶囊式的导航   需要依赖.nav
.nav-stacked 

.nav-inverse 表示背景色为黑色的导航
.nav-aside 表示侧边栏导航
.nav-fixed-top 表示固定导航 在顶部
nav-fixed-left 表示 屏幕左边固定导航
.nav-fixed-right 表示 屏幕右边固定导航


### 导航条 .navbar
注意：兼容移动端 
兼容移动端样式设置规则：媒体查询最小宽度；写pc端样式；当小于这个宽度时候；使用浏览器默认样式
网站的导航条；到移动端时候可以折叠 

.navbar  导航条 兼容pc 移动  默认样式隐藏
.navbar-default 给导航条添加样式  背景色
.navbar-header 有媒体查询样式；做PC 端和移动端区分； 移动端宽度100%
.collapse  元素隐藏[移动端]
.nav-collapse.collapse 在pc 端【强制】显示
.navbar-nav 表示导航条下导航
.navbar-form 表示导航条中输入框
.navbar-left 让导航在导航条中左浮动【移动端无浮动】
.navbar-right 让导航有又浮动【移动端无浮动效果】
.navbar-toggle 表示显示隐藏列表导航栏，有【右浮动】效果

.navbar-fixed-top 固定顶部导航条
.navbar-inverse 黑色导航条 border-bottom:1px solid black
   .navbar .active  背景颜色黑色  字体白色

 .breadcrumb 表示路径导航；没有基础类  

  - 每个a 添加伪元素； content:"Z/\00a0"


## 规范：
1： 清空所有html标签的默认样式
2： 字体： 标准14px  最大  36px  最小12px

3： 布局  栅格系统 ： 给一个父容器 等分多少份

最小分为
12列：
每个子元素可以占12列中  1-12份  最大为12份
col-12 占据12份   


### 表单样式组件
1只有表单元素 分为基础元素与可选择元素 如有特殊需要 请自定义
2.表单没有进行验证处理 有对验证效果样式处理 statice状态
3.表单验证需要JS 正则完成 注意 正规规则必须写基础正则不要写新的正则 因为IE和火狐部分版本不兼容
#### 表单组件基础样式
.form-group 表示 表单组件
.form-control 表示表单控件
.form-label 表示input 的提示信息只能应用在label标签中

##### 可选项表单样式
.form-inline 表示横向的表单 
.form-horizontal 是纵向表单

#### 表单中控件
.form-check 选择项组件 在ul中使用
.form-check-item 表示多选项 在li中使用
.form-content 表示选择的文本描述


#### 栅格系统 .col
栅格系统 是横向布局的处理
如果 父容器：不适用.row 那么自已清除浮动 计算父容器的高度

#### 容器 .row
将.row 容器分为12份

#### 屏幕
.col-xs-xx  768 以下尺寸
.col-sm-xx  768以上 992以下
.col-md-xx  992以上  1200以下
.col-lg-xx  1200以上



#### 分的份数  小数点后7位数
1. 8.3333333%
2. 16.6666667%
3. 25
4. 33.3333333%
5. 41.6666667%
6. 50
7. 58.3333333%
8. 66.6666667%
9. 75
10. 83.3333333%
11. 91.6666667%
12. 100

#### 列偏移
通过改变position：relative Left 实现列偏移
*表示1 2 3 4 5 6  7 8 9 10 11 12
.col-xs-offset-*
.col-sm-offset-*
.col-md-offset-*
.col-lg-offset-*
#### 偏移量
1
2
3
4
5
6
7
8
9
10
11
12


#### 排列
.col-xs-pull-* 相对元素位置右边多元（往做走）
.col-xs-pull*  往右边走





### 开发浏览器注意事项
1  如果你是IE7 8 请更换浏览器
2  IE7尽量全部使用div 例如
   - ul  div.ul
   - li  div.li
   - span  div.span  设置 display: inline;
3  IE78 不支持 浮动 清除浮动  css3  百分之90属性
