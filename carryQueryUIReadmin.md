# carryQueryUI 全局样式说明文档
## 清空默认样式



## 布局
.container  设置为容器：水平方向居中。宽度部位100% 左右内边距为15px 高度没有
.container-fluid  宽度为100% 的容器 没有外编辑；内边距左右15px 上下0px  没高度






## 按钮  -btn
#### 普通的按钮样式
成功  btn-success 
f警告  btn-warning
错误  btn-error
取消  btn-cancel
确认  btn-sure
默认  btn-default
危险   btn-danger
首选   btn-primany
一般信息  btn-info
百搭按钮  btn-normal
暖色按钮  btn-warm

#### 渐变的按钮样式
成功  btn-success-rgb 
f警告  btn-warning-rgb
错误  btn-error-rgb
取消  btn-cancel-rgb
确认  btn-sure-rgb
默认  btn-default-rgb
危险   btn-danger-rgb
首选   btn-primany-rgb
一般信息  btn-info-rgb
百搭按钮  btn-normal-rgb
暖色按钮  btn-warm-rgb

#### 伪类按钮样式



- 型号
大  btn-bg
小  btn-sm
中  btn-md

- 圆角按钮 btn-radius

## 表单

## 滑块

## selec选择框

## 表格 .table
.table 表示基础表格；必须在table标签中使用；表示只有列边框的表格
.table-striped 表示条状表格；表体的偶数行；有一定的背景颜色
.table-column 表示半边框样式
.table-hover  表示悬浮表格
.table-condensed  表示紧缩表格
.table-border  全边框表格
.table-inverse  背景颜色为黑色表格
.table-inverse-striped 黑色条形表格
.table-inverse-hover 黑色悬浮表格 需要依赖.table-inverse 或者.table-inverse-striped
.table-control  表示控制列固定 其他列可以滚动   .table-control必须给table标签的祖籍元素添加；不能给父元素添加
~~~css
.table-control{

}
.table-control table>tr>td:last-child{
    position:absolute;
    rigth:0;
    min-width:120px;
    text-align-center;
    box-shadow:-5px 4px 6px 1px #ccc;
}
/* 选中倒数第二个列：解决内容遮罩问题 */
.table-control table>tr>td:nth-last-child(2)::before{
    content:"";
    width:120px;
}
.table-control>.table-box{
    overflow:auto;
}
~~~


.table-responsive  移动端表格：可以有横向滚动的效果  .table-reponsive 需要给table的父容器添加


状态表格：给tr添加类名
.success 成功
.info   通过
.warning  警告
.danger 危险
.primary 首选
.warm   暖色

## 栅格系统

## 分页.Page
.pagination 实现分页样式 有ul li a完成分页效果
.pagination-bgc 表示带有背景颜色
.pagination-noBgc 
.pagination-inverse 黑色分页 14px padding 5px 10px
.pagination-inverse-lg  16px字体大小  padding 8px 12px


## 表单类

### 单选或多选框样式    
.circle-check 圆形选择框  .circle-check  需要给input[type="checkbox"]的父元素添加   
.square-check 方形选择框  .square-check   需要给input[type="checkbox"]的父元素添加
~~~css
  <div class="circle-check">
        <input type="checkbox">
    </div>

    <div class="square-check">
        <input type="checkbox">
    </div>
~~~


### 滑块 .sliderbar
.sliderbar-wrap 表示进度条外围容器
.sliderbar 表示 滑块条
.sliderbar-control 表示控制键

~~~html
<div class="sliderbar">
        <div class="sliderbar-control"></div>
    </div>
~~~

状态
.sliderbar-success
.sliderbar-info
.sliderbar-primary
.sliderbar-error



### 开关  .swich
.swich 开关样式的选择框需要给   <input type="checkbox" class="switch"> 才能实现
    -绿色开 input=checkbox  灰色为官  input = disable

状态
.swich-info  蓝开  灰关
.swich-danger 红开 灰关
.swich-warm  橙开   灰关
.swich-primary  蓝开 红关


### 步骤组件step
.step-wrap  为外部容器55rem
.step-full  每个步骤容器包含内容：圈 线 文本
.step 具体进行的每一步 用input[type = checkbox], 当有checked 属性表示当前步骤已经完成。
.step-circle  表示圈
.step-line  表示线
.step-text 表示步骤内容


状态
.step-circle-info
.step-circle-success
.step-circle-primary
.step-ciecle-warm
.step-ciecle-error
.step-ciecle-danger


### 导航 .nav
注意：导航仅仅只用于pc端应用：且只适用与静态样式，导航中所有的样式都是操作li下的a标签
.nav-tab 表示想tab样式的导航条  需要依赖.nav
.nav-pills 表示胶囊式的导航 需要依赖.nav
.nav-stacked 


.nav-inverse 表示背景色为黑色的导航条
.nav-asid   表示侧边栏导航
.nav-fixed-top  表示固定导航在顶部
.nav-fixed-left  表示固定在左边的导航
.nav-fixed-right  表示固定在右边的导航



### 导航条 .navbar
 兼容移动端样式设置规则：媒体查询最小宽度；写pc端样式；当小于这个宽度时候；使用浏览器默认样式
网站的导航条；到移动端时候可以折叠 

.navbar  导航条 兼容pc 移动  默认样式隐藏状态
.navbar-default 给导航条添加样式【给背景色】
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
1：清空所有Html标签的默认样式

2：字体：标准 14px   最大 36px  最小 12 px 


3: 布局 栅格系统  ：给一一个父容器 等分多少份?
    12列：
    每个子元素可以占12列中 1-12 最大为12分
    col-12 占据12份



### 表单样式组件
1、只有表单样式，分为基础样式与可选样式    如有特殊需要请自定义
2、表单没有进行验证处理     有对验证效果样式处理:statice状态
3、表单验证需要js  正则完成   注意：正则规则必须写基础正则不要写新的正则 因为ie火狐部分版本不兼容
### 表单组件基础样式
.form-group 表示表单组件
.form-control 表示表单控件
.form-label 表示input的提示信息只能应用在label标签中


### 表单中控件
.form-check 选择项组件  在ul中使用
.form-check-item 表示多选项 在li中使用
.check-content 表示 选择的文本描述


### 可选项表单样式
.form-inline 表示横向的表单
.form-horizontal 纵向表单




### 栅格系统 .col
栅格系统 是横向布局处理
如果父容器：不使用.row 那么自己清除浮动   计算父容器高度


#### 容器 .row
将.row 容器等分为12份


#### 屏幕
.col-xs-xx   < 768px
.col-sm-xx    
.col-md-xx    992px<=
.col-lg-xx    1920px<= 


#### 份数
1份 8.333333%
2份 16.666667%
3份 25%
4   33.333333%
5   41.666667%
6   50%
7   58.333333%
8




#### 列偏移
通过改变position:relative left 实现列偏移

xx:1-12

.col-xs-offset-xx
.col-sm-offset-xx
.col-md-offset-xx
.col-lg-offset-xx

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


### 排列
.col-xs-pull-xx相对元素位置右边多远（往左走）
.col-xs-push-xx 