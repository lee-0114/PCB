[toc]

# 无模命令

logic中搜索：s +元件名，S jp3

LAYOUT 中搜索：ss +元件名  如ss jp3，搜索jp3

N +网络名就可以高亮，右键选择网络，选中该网络，ctrl+u取消高亮

PO切换覆铜，如果不行，比如内层，电源层和地层，PO不能去掉，就用SPO，因为在叠层中设置了混合/分割

Q快速显示长度

QL，选中网络，QL，会出长度报告

最小显示宽度，R 0，

设置原点：输入S O，按空格

ZU关闭飞线或者打开飞线

关闭某一网络线或者类飞线

![image-20200804104340519](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804104340519.png)

# 操作

layout中选中元器件，ctrl+h可以亮选

如果其他如AD、orcad等要导入到pads中操作，首先打开，原理图和PCB新建保存库，然后加载库，打开文件

如果只有PCB，导入的时候直接两个全部打勾！！！

异形焊盘，将规则的和不规则的焊盘右键关联

pads导出asc文件，AD可以导入asc文件！！！

shift+Z可以单端走线，差分网络应用

# 工具

snagit  截图软件，也可以截视频

# 快捷键设置

快捷键设置总结：

1是设置颜色

2是设计规则

3是验证设计

4是覆铜平面管理器

5是查看网络，给网络分配颜色等

F是筛选条件

J是亮选

x是修线





空白处----右键---自定义---键盘和鼠标

//布线：所有模式----设计工具栏------添加布线----F，原来是F2，用来布线

拉线：所有模式-----其他命令----拉伸，设置为X，原来是shift+s

删除线：

操作无效时，可能是wox和everything引起的冲突

一般layout中设置如下快捷键：

亮选：J   所有模式----编辑----亮选

![image-20200803141134292](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803141134292.png)

筛选条件：F   所有模式----编辑----筛选条件

![image-20200803143536316](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803143536316.png)



网络：查看----网络  5 

![image-20200803143814784](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803143814784.png)



设计规则：设置----设计规则

![image-20200803144014107](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803144014107.png)



设置颜色，显示颜色：1   设置----显示颜色

![image-20200803143957212](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803143957212.png)

验证设计：3   工具---验证设计

![image-20200803144132225](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803144132225.png)

覆铜平面管理器：4    工具-----覆铜平面管理器

![image-20200803144210765](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803144210765.png)

# 说明



规则在全局的权限之上

12/24mil  刚好是0.3/0.6的孔

# 关于库制作说明

可以保存PCB文件，或者制作库文件，然后需要的时候打开保存到新建的项目库。

保存库的时候，原理图全选保存

PCB全选，保存到库中，如果是对应logic原理图，一般logic不保存，只保存封装

![image-20200802222442160](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802222442160.png)



# logic设置

## 1、ctrl+enter 设置----选项，常规设置：

<img src="C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200801160154600.png" alt="image-20200801160154600" style="zoom: 67%;" />

<img src="C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200801160229243.png" alt="image-20200801160229243" style="zoom:67%;" />



元件中，REF是位号，PART-TYPE是类型

## 做逻辑库：

1、设置参数，设置格点 G 50,GD 50

2、设置好库，存放的地方

3、新建元件，手动画或者向导

## 做元件库

元件库里面的编辑电参数------门----双击CAE封装

![image-20200802115915857](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802115915857.png)

选择逻辑里面的封装，然后确定，选择管脚，因为有8个引脚，所以添加八个引脚

![image-20200802120125826](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802120125826.png)

或者选择下面那个添加管脚，可以批量添加

属性可以添加一些信息，如公司名称等

然后点击左下角检查元件！

## 8、多gate元件库创建

画的时候输入R 0就可以显示宽度

先创建逻辑库元件，画LM358的分立模块

画完之后去元件库添加门，然后添加管脚，注意对应

==如果需要更改元件的地方，直接编辑逻辑库里的元件，修改后会自动同步==



## 9、利用excel表格创建元件库

==使用excel的时候注意切换到英文界面才可以！！==

工具-----自定义----选项-----界面语言

引脚多的如FPGA可以从官网上下载对应的引脚图，放到EXCEL中

![image-20200802143056009](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802143056009.png)

先添加门，然后选择引脚，导入CSV

![image-20200802143144426](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802143144426.png)



## 10、从已有的原理图中保存元件库

打开原理图-----右键---选择元件-----选择元件右键----保存到库中。

在左侧的项目浏览器中，打开元件类型，选中第一个，然后shift+最后一个， 右键保存到库中

## 11、新建和添加原理图

设置-----图页

里面可以修改名称和添加图纸

## 12、添加元件到原理图库中

绘图工具栏----添加元件----添加

如果要隐藏某一些属性，可以双击元件，然后可见性，自行设置

## 13、添加总线

工具栏----添加总线-----形式是D[0:7]，可以修改总线，延伸，分割

## 14、显示网络名

在连线的靠近引脚的地方双击才可以显示

## 15、导出BOM表

文件-----报告-----材料清单---设置

![image-20200802165742311](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802165742311.png)

除此之外，还可以有制造商、说明、value、PCB decal、description说明

## 16、导出PDF

1、文件-----生成PDF，可以输出有电气特性的PDF文件

2、文件----打印，选择相应大小的纸张，输出PDF

## 17、将原理图导入到PCB

![image-20200802224035795](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802224035795.png)

![image-20200802224047914](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802224047914.png)

![image-20200802224115085](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802224115085.png)

### 导入库padsnet.err文件说明

一致性检查报错，如红色框部分是错误的部分，意思是说元件logic中jp3，多了两个引脚，在PCB封装JP3中没有找到7和8脚，解决方法是打开logic编辑查看JP3的管脚，可以把7和8删了

即logic中有6个引脚，PCB也是6个，但是元件库里面有8个管脚

![image-20200802224345727](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802224345727.png)

![image-20200802225000488](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802225000488.png)

删除后再次发送网表：

![image-20200802225251722](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802225251722.png)

上述错误是因为有两种封装：

![image-20200802225637712](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200802225637712.png)

JP3和JP3B两种封装，查看可以知道JP3B是8引脚的

查看logic和pcb里面导入的封装和原理图一致，所以这个错误可以忽略。

一般来说如果==设计与库元件的一致性检查==这个错误解决了，就说明元件全部导入了





## 20、layout介绍

### 常规设置

#### 设计

ctrl+enter打开设置---设计，红色框内打勾的话，移动器件的时候，线会跟着走，不勾的话，线会停留在原地，不会导致线推挤的情况，常规可以不勾

![image-20200803100005455](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803100005455.png)



倒角：比如铺铜的时候是正方形/长方形，然后画完右键----倒角，设置半径，就可以把角去掉，变成斜角或者圆弧之类的，看选项



![image-20200803100252020](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803100252020.png)

#### 栅格和捕获

绘图工具栏-----铜箔，画一个方形，然后确定，右键选择形状-----选中，右键，添加倒角，输入半径、

![image-20200803100646324](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803100646324.png)

![image-20200803100640405](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803100640405.png)

如上图，添加了倒角



设置----栅格----铺铜栅格---一般铜箔设置为4

铺铜栅格：铺铜的宽度

铜箔有宽度，比如1，铺铜栅格设置为4，那中间就会有3个格是空出来的

铺实心铜：把铜箔的宽度设置的比铺铜栅格数值大或者等于即可

禁止区域：原来设置为100，绘图工具---禁止区域，默认画出来是4，如下

![image-20200803101404444](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803101404444.png)

将禁止区域设置为3：

![image-20200803101506168](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803101506168.png)

![image-20200803101512661](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803101512661.png)

不产生实际的影响，只是显示效果的问题

##### 对象捕捉

一般不打开，会去捕捉点，除非导入板框之类要固定位置，对齐，捕捉到某个地方

#### 布线

层设置top和bottom，还有生成泪滴，看需求

![](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803101918209.png)

#### 铺铜平面

设置如下

![image-20200803102454753](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803102454753.png)

第二项勾选的话会出现很多xxx，对于看图影响大，也不要移除没有使用的焊盘

下图平滑半径要改为0，不为0会影响覆铜效果，可能导致一些地方没连接上。

![image-20200803102557018](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803102557018.png)

#### 尺寸标注/文本

![image-20200803112541324](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803112541324.png)



## 21、颜色偏好设置

参考编号是位号即R1这些，管脚编号是1、2、3这些

## 22、layout快捷键设置

## 23、导入DXF

文件----导入-----选择DXF文件

选择公制，做结构的工程师都是用mm单位去做的

![image-20200803150523050](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803150523050.png)



导入的板框要是四方闭合的，没有多余的线头出来，也没有缺口，不然选择形状，特性是更改不了为板框的

导入的板框在用不到的层，不要放在信号层！！

## 24、利用AD软件导入板框结构图

AD绘制板框，或者导入板框DXF，然后保存pcb，用pad layout打开，然后复制层

如果拷贝不过去，是因为保存的pcb层数和需要做的pcb层数不一样，设置-----层定义----最大层，两者都开到最大层就可以了

## 25、交互式LOGIC和layout

如果要同步AD或者orcad的原理图和PCB，可以先导入原理图，生成.sch和.pcb的文件，然后同步

## ==30、将AD，orcad原理图导入到pads layout中==

### orcad导入步骤

1、先将封装库加载到layout中，即加载库，如果没有库，可以打开PCB，然后导入，保存到库里面，元件库和封装库都要保存

2、打开orcad 原理图，create netlist 创建网表----other，选择orpads2k.dll，生成asc文件

3、打开layout，新建，指定好库，文件----导入-----asc文件，确定，即可导入

### AD导入步骤、

1、准备好原理图，PCB文件，创建layout库文件，加载库

2、打开素材的PCB，即可以调库的文件，选中元件，保存到库中，元件类型和封装都要选上！！！

3、打开AD软件，新建工程，把原理图放进去，然后 设计-----从工程生成网表 ------PADS

生成.net和.PRT文件，参考orcad文件的asc文件，用记事本或者其他notepad打开asc，参考。

.PRT文件也是part，如下图，是asc文件的整体

![image-20200803193403067](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803193403067.png)

把net文件里面的网络放到asc文件里面的网络NET下面，把.PRT文件放到元件部分part部分

4、打开layout，指定好库，导入asc文件





将AD原理图导入到pads layout中称之为导网表，导网表，首先要将封装库加载到库里面



个人理解：是在只有pads库和原理图的情况下，将其他如AD，orcad的原理图，转换成pads layout的pcb，可以直接布局布线

很多公司是用orcad去做原理图，然后用layout去做pcb的。！！！！

## 31、ECO功能更新PCB

什么时候用到ECO：

1、原理图不是用logic做的

2、原理图用AD或者orcad做的，然后原理图有改动的情况就需要使用ECO功能

用更改后的原理图，导出新的asc文件，保存为ref.pcb文件，即参考的PCB

然后在layout中用eco功能去比对，工具-----对比eco

![image-20200803182435947](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803182435947.png)

![image-20200803182648828](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803182648828.png)

然后运行，显示报告看，可以看到差异。

然后关闭，打开文件----导入-----ECO文件即可。



## 33、叠层设置及修改

设置-----层定义，默认2层板

![image-20200803194606612](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803194606612.png)

一般默认即可，平面类型，top和bottom都是无平面，CAM平面式负片层（一般不用），分割/混合，一般用在GND层和电源层

如果选择了CAM平面/分割，混合，需要分配网络才可以分配，一般默认无平面即可，效果是一样的。

![image-20200803195427620](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803195427620.png)



四层变两层，把线之类的都删了，再改成2层，减层是需要去删除层里面的东西，不然会报错！！！

关闭某层，设置-------层定义------启用/禁用

## 34、过孔Via添加以及修改

设置----焊盘栈

一般有如下的大小：12/24，10/22，8/16，8/14四种选择

一般选择大孔，载流能力强，成本低



![image-20200803200528910](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803200528910.png)



设置好之后，设置----设计规则-----默认规则-----布线

![image-20200803200652800](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803200652800.png)

选定的孔中添加，然后确定。

布线的时候，右键----过孔类型，可以选择其他过孔！！！！

更改过孔：右键-----过滤器----筛选，过孔和缝合孔，然后选择孔，右键，特性选择其他的孔即可

## 35、虚拟过孔功能介绍

和过孔的区别主要是：右键选择管脚对的时候，会分开，而过孔不会分开。

![image-20200803214717175](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803214717175.png)

普通过孔，选择导线，选择管脚对，是全选的，选中是黄色

![image-20200803215025567](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803215025567.png)

虚拟过孔，选择导线，选择管脚对，只选择了一边，相当于分开的，选中是黄色

![image-20200803215901376](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200803215901376.png)

主要用到T型结构里面，拓扑结构，做等长的时候

拓扑结构：1、T点结构，T型

2、菊花链  fly-by，串起来

做完等长之后，可以选择虚拟过孔，右键，转换为过孔！！！



## 36、常规线宽、间距规则的设置

设置-----设计规则----默认规则 ，根据PCB板厂的生产能力，走多粗的线可以用SI9000计算

铜箔到铜箔距离可以设置大一点，如15mil，一般是电源到电源才会用到铜箔

板到其他地方都可以设置为20

一般设置如下

![image-20200804095317159](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804095317159.png)

### DRC规则设置

![image-20200804095610094](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804095610094.png)

### 打孔设置

在类里面可以指定特殊的孔大小。安全间距----布线里面设置

   

### 添加类

选择网络，右键添加类

或者打开规则设置，类，添加

## 38、不同层的规则设置

所有层都是基于默认规则的，但是有要求设置某一层，可以单独设置

比如第三层通过叠层计算出来其他线宽才是50欧姆的阻抗，需要单独设置第三层

设置-----设计规则-----条件规则，如下图

对某一层，点击，创建，选中网络集，矩阵，就可以单独设置规则，对于类或者其他也一样，一般设置线宽，间距，板框

如内层要内缩就可以这样做，电源层内缩，然后外面一圈打上地，这样可以减少干扰

![image-20200804101833910](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804101833910.png)

关闭某一类/网络线：如下图，一个是关闭，一个是打开

![image-20200804104355624](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804104355624.png)

## 40、器件移动、旋转的方法

如下图可以按照设置去移动

![image-20200804104730231](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804104730231.png)

选中 tab旋转

选中移动，ctrl+e，切换到背面：ctrl+f

## 41、group组的添加以及打散

选中元器件，选择模块（一部分电路），右键创建组合，可以整体移动，旋转等

选中group的方法：1、选择里面某个器件，然后右键，选中组合

2、过滤器选择组合，选择里面某个元件

打散：选择元件，右键，打散

如果不想移动器件可以创建组合，即固定部分

## 43、器件的打孔以及IC扇出操作

上下对齐，左右对齐，器件对称，打完孔可以拷贝

![image-20200804141944925](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804141944925.png)

电源信号扇出，尽量在管脚附近，不要离很远，电源信号干扰。

![image-20200804142328834](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804142328834.png)



## 44、添加、编辑铜箔功能介绍和覆铜平面的区别

铜箔绘制出来时不会避让的，比如你画了多大就是多大，旁边有线也不会避让

而覆铜平面是会避让的，覆铜平面需要灌铜才会显示

常规下覆铜的时候选上过孔全覆盖，在灌注 填充选项里面，里面还有灌注优先级，数字越小，优先级越高

有两个铜皮相交在一起的话要设置优先级别，先铺优先级低，再铺高的，==越里面的铜皮设置数字越小！！==

铜箔挖空区和覆铜挖空区是对称的，如果需要挖空哪里，可以画，然后和铜交叉的地方选择合并即可。

## 45、reuse功能介绍

把某一部分模块通过reuse拷贝到同一个板子上，可以分工，每个人做一个模块，然后拷贝。

1、首先保证两个板子的层数是一样的！！都设置为最大层。同样是4层板或者6层板

2、在副板上设置原点，主板上也设置，如芯片的同一个引脚上设置，然后把副板的元件位置XY对应到主板的位置，移动。然后打开过滤器，打勾需要拷贝的东西，把格点设置大点，如100

3、选中要拷贝的东西，右键-----建立复用模块，名字，确定，放到某个位置。

4、去主板中，设置格点，ECO工具，添加复用模块。全部确定，不用管即可拷贝过来

5、注意：有过孔的话，主板上需要有副板上的过孔类型，不然拷贝不过来

6、主板上过滤器，选上复用模块，选中，右键，打散，就可以操作某一条线了

什么时候用：

模块是一样的，如新的设计里面有参考板里面是一样的，或者多人协作的时候

条件：

1、层一致

2、过孔要设置好

3、要去过滤，选择要的元素

4、把原点设置好，设置同一个位置

5、格点设置大一点如100

6、复用模块要编辑需要打散

## 46、宏命令的添加以及使用介绍

如每次新建PCB都要设置东西，这时候可以录制成一个宏

打孔等也可以设置为一个宏

![image-20200804155307521](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804155307521.png)

## 47、连接性DRC验证以及消除

遇到线已经连接上的，但是还是报错的地方，把该网络的线删除，然后重新布线。

## 48、安全间距DRC验证以及消除

设置好要检查的东西

## 49、丝印调整、字符添加、logo导入

打开相应的层和丝印层，solder层，分配颜色，关闭线，孔、铜箔之类的，打开选择器，然后只选择标签，全选，右键，特性，然后输出想要的大小尺寸，位置

器件丝印top层：从左到右R50，从下到上

bottom层：从右到左如05R，从下到上

如果需要修改封装的丝印，选中元件，右键编辑封装，然后修改位置，然后确认，弹出：保持现有属性，已选定。

50/5，添加文本的话可以50/10

==检查丝印有没有全部调完，打开选择器，只打开元件，crtl+h高亮，看到全部高亮完就证明全部调整好==了。

丝印不小心被删掉的话：

选择元件，右键特性----标签，新的，ref.des，层位置即可



logo一般放在封装库里面！layout打开ECO工具，确定，然后选择添加器件，选择相应的库，器件即可。

## 50、间距测量、尺寸标注功能

layout中尺寸标注工具栏，可以选择水平或者垂直测量，精度在选项里面设置。

要测量什么，就在选择器里面打开某一个，测量的层放到最后一个层

一般测量用mm单位

1、精度

2、过滤选择

3、水平/垂直，选对测量工具

4、右键捕获中心

5、选择元素

6、板框一般公制 放dill层

## 51、光绘文件

原点设置在左下角，先覆铜，然后检查连接性和间距，没有错误之后

文件-----CAM

偏移量所有层都要设置相同，不然检查人员需要重新设置，焊盘尺寸大小一般内层可以 稍微放大，默认也可以

![image-20200804204311719](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804204311719.png)

下图设备设置----高级----一般默认就可以

![image-20200804204539855](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804204539855.png)



重要设置：如下图，1、2、3

一般1部分默认只出板框就可以

2部分是在出丝印层的时候才会用到，所以其他层都可以不选

3部分解释：下面的都是基于TOP层的

焊盘是贴片封装那些焊盘

导线是router里连接好的线

2D线绘制的一些2D线，如果是top和bottom层，画出来是铜皮的形式，如屏蔽罩。

过孔是打的过孔，铜箔同

参考编号是指R1、R2、C3这种，一般也是丝印层才出

元件类型就是value值，一般不出，是出PDF的时候可以用

文本就是添加的text，如果有就可以出

属性是一个器件有多高，或者其他的tag，一般不出，除非有特殊要求

边框是top层的边框，根据实际情况

测试点不是器件的tp点，是手动添加的一个测试点，如果有添加就勾上

具有关联覆铜的管脚：异形焊盘的时候，一般会选上，在top和bottom都选上，会用在阻焊层和钢网层

![image-20200804205613983](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200804205613983.png)

## 52、光绘平面层设置

出光绘要设置的层 

1、几层板就几个平面

2、两层顶底阻焊层

3、两层顶底钢网层

4、丝印层

5、钻孔层

6、NC钻孔层

CAM平面是负片工艺，布线/分割平面是正片工艺

光绘文件可以用CAM350打开

2D线是TOP层，即铜皮的，有屏蔽罩之类的需要勾上，2D线和文本一般顶底层是没有的，勾上也没事

![image-20200805135108390](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805135108390.png)

## 53、光绘丝印层设置

![image-20200805135519898](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805135519898.png)

![image-20200805135824341](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805135824341.png)

![image-20200805140013300](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805140013300.png)

如上图，名称可以设置为ST,SB.TOP和silkscreen TOP层的设置，参考编号如果在密度很高的情况下，没有位置放置了，可以不打印出来，具体根据实际情况 ，bottom层也是一样。

## 54、光绘阻焊层添加设置

阻焊层名称可以设置为SMT

下图设置的大5mil，如果是mm单位，则写0.127，阻焊是绿油

2D线，有屏蔽罩的时候会用2D线绘制，露铜的区域，一般可以勾上。

==过孔选项==：如果板子上的过孔需要阻焊开窗，即过孔露出来，就勾上。不需要就不勾

![image-20200805140413725](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805140413725.png)

![image-20200805140519304](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805140519304.png)

![image-20200805140617319](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805140617319.png)

## 55、光绘钢网层添加设置

名称是PMT,PMB



![image-20200805145230807](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805145230807.png)

![image-20200805145244453](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805145244453.png)

![image-20200805145256853](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805145256853.png)

## 56、光绘drill drawing层设置

名称，DD

文本是标识

如下图，第一张有紫色框，需要把预览里面的紫色框放到蓝色框外，设置偏移。然后点击钻孔符号，得到第二张图，把原有的全部删除，然后重新生成，保存！

![image-20200805145720680](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805145720680.png)

![image-20200805150014288](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805150014288.png)

![image-20200805145515271](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805145515271.png)

![image-20200805145530910](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805145530910.png)

## 57、光绘NC Drill层设置

名称是NC，设置如下。

![image-20200805150155414](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805150155414.png)

## 58、导出IPC网表

导出的网表是给PCB板厂检查有没有开短路。将IPC网表导入CAM文件里面去对比

文件-----导出-----IPC356文件，.ipc

![image-20200805150657049](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805150657049.png)

![image-20200805150630777](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805150630777.png)

## 59、导出器件贴片坐标文件

这个文件是某个器件放到PCB上的某个位置，XY位置，给贴片厂，去抓取器件，放到某个位置。即给机器去抓取元件放到相应的位置。

工具------基本脚本-----17，运行生成EXCEL表格，导出来的表格单位是mil单位的

如果需要mm单位的，就使用 umm切换单位，再次导出即可。

如果因为驱动或者其他原因生成不出来，那就发给其他人电脑，去运行一下，跟系统有关系。

![image-20200805151053756](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805151053756.png)

## ==60、光绘文件生成以及检查==

使用CAM350去检查，导入光绘文件

1、检查各层有没有显示，空白就有错误

2、检查丝印有没有上阻焊（不允许）

3、检查有没有焊盘有没有缺少阻焊，把贴片层，PMT和SMT文件进行比对，钢网层和阻焊层打开比对一下

下图是丝印上阻焊和检查焊盘有没有缺少阻焊层

![image-20200805155557328](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805155557328.png)

![image-20200805155533178](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805155533178.png)

![image-20200805155739982](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805155739982.png)

## 61、利用光绘模板文件添加光绘

即将以前设置好的CAM文件模板保存起来，下次遇到相同的层数可以采用模板，不用一个个去设置。检查即可，但是对于DD过孔，钻孔层，要把钻孔符号全部删掉，然后重新生成。

记得设置层数一样和最大层数一样！！！

1、导入

2、检查选项

3、钻孔删除，重新生成

4、保存，相当于设置好了。

综上，做板子的时候把各层的CAM文件都保存，然后需要的时候导入模板即可

## 62、输出器件装配图PDF

设置如下：可以勾选调整为合适大小！！

常规情况不显示焊盘，密度太大的话丝印没地方放

![image-20200805160059026](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805160059026.png)

![image-20200805160112024](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805160112024.png)



![image-20200805160601044](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805160601044.png)

![image-20200805160612105](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805160612105.png)

![image-20200805160659187](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805160659187.png)

## 63、文件分类及归档

一般有ASM、CAM、SMT、PCB、SCH、LIB、NOTE、DXF文件

PDF文件放ASM

PMT、PMB、SMT、SMB、坐标文件，放到SMT文件夹

gerber除去PMT、PMB、SMT、SMB，再加个ipc网表就是CAM文件

板框放DXF

PCB放PCB文件夹

NOTE是说明，设计要求等。

制板就把CAM压缩，加上工艺说明发给板厂。

## 66、router参数设置

如下，1是可以在一条线上拉出多条线，不会消失，2是做盲埋孔设计才用到，3是拉线的时候其他线可不可以推挤。

![image-20200805215648586](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805215648586.png)

调整这里改为3就可以，这是做等长的时候三倍线宽的！！！

![image-20200805215844631](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805215844631.png)

验证设计

![image-20200805220035559](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805220035559.png)

## 68、打孔常用命令

## 69、自定义快捷键设置

![image-20200805221655522](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805221655522.png)

## 70、BGA元件扇孔功能介绍

把有信号的引脚一次扇出来

一般BGA 横向和纵向间距是一样的

1、测量两个焊盘之间的距离，设置好精度

2、格点设置为间距的一半！！

25.59mil是0.65mm的间距，0.65的间距只能添加8/14的孔 

==不同引脚的间距选择的过孔不一样：1mm的选8/16的，0.8mm选8/16的，0.65的选8/14的，0.5及以下的是打不了孔的，只能激光打孔==

3、扇出前先把规则删了，然后设置为线做的线宽。新板子的话默认是空白的规则

设置好过孔

router中是没有设置原点的功能，在layout中要 设置好！！

4、打开router，然后双击空白处打开设计特性，选择扇出，如下设置

扇出之前打开所有层，ZZ看看器件底下有没有东西，有器件会DRC报错，可能会不成功

5、右键，选择元器件，选择元件，右键，扇出，如果遇到线很细的情况，R 0一下

![image-20200805225257558](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805225257558.png)

![image-20200805231009985](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200805231009985.png)

## 71、覆铜平面功能介绍

router中铜皮不能倒角，要去layout中才可以

## 72、添加差分对及其规则设置

差分对走线是耦合的，线间距处处相等，长度差需要在5mil内，一般用在高速信号上，运行的速率比较高。

差分对首先需要知道线宽和间距是多少？这个是根据叠层算出来的一个线宽间距，从板厚和板层算出来的。

多少欧姆的阻抗，如100，50，一般是有要求的，比如USB的信号是90欧姆的阻抗，常规是100欧姆的阻抗

在router中建立差分网络，右键选择网络，选择两个网络，然后右键建立差分网络。在项目浏览器中就可以看到。

然后设置差分对，右键要设置的差分对，特性

叠层设置如下图，第三层是4.5/9，其他都是4.1/8.5，可以添加层，再设置

shift+Z可以单端走线

差分信号速率是比较高的，要保证回流路径短

需要换层，就可以在差分信号附近打地孔，增加回流路径，一般是信号到地。一个信号进来，回流到地。

不打孔和打孔信号质量相差很多。

高速信号换层的时候要打过孔，GND的过孔。

![image-20200806095852868](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806095852868.png)

![image-20200806095950085](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806095950085.png)

![image-20200806100247618](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806100247618.png)



## 73、蛇形等长组的添加以及绕绘介绍

1、做等长，一定要先把信号线连通了再做等长！！！

2、电子表格双击可以排序。

3、手动或者软件绕线，设置格点！！修线

手动要修线，设置好格点，保证美观

软件画线shift+A，边走边看表格里面数据的变化。

4、高速PCB肯定涉及到等长，记得设置3W线宽，最少最少是2



要做等长，选中网络，右键，建立匹配长度的网络组

绕等长的时候最好方方正正，和角度一样高

绕的时候尽量在直的地方绕，斜的地方不好绕

有手动绕和软件绕，手动是自己看位置，修改格点为5，然后绕到等长

软件绕线的话：先建立等长匹配网络，然后看在直的地方，选择要走蛇形的的地方，然后布线，shift+A（右键---添加蛇形走线），然后走蛇形，结束的话就右键，完成蛇形走线绘制，即可。

记得设置最小间隙为3，即3W的规则。

如下

![image-20200806102209391](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806102209391.png)

![image-20200806105440008](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806105440008.png)



3W是调整1和2之间的宽度。



![image-20200806105747313](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806105747313.png)

![image-20200806105838425](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806105838425.png)



手动绕的时候如果遇到下列情况，闭合的地方没有消失，可以去设置里面修改，如下，不勾允许回路即可

![image-20200806111641003](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806111641003.png)

![image-20200806112051273](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806112051273.png)

![image-20200806112145808](C:\Users\13544\AppData\Roaming\Typora\typora-user-images\image-20200806112145808.png)



## 76、手动绘制封装

单位MM

通孔增加0.2左右，长度增加1.2左右

选中引脚，分布和重复，可以复制出来

## 80、布局得基本原则介绍

模拟信号一般是小信号，电流比较小，容易受到干扰，模拟信号和数字信号分开，防止数字信号干扰模拟信号

电源电路和模拟电路保持一定距离，防止干扰

接口保护器件摆放顺序要求：
（1）一般电源防雷保护器件的顺序是：压敏电阻、保险丝、抑制二极管、EMI滤波器、电感或者共模电感，对于原理图缺失上面任意器件顺延布局；
（2） 一般对接口信号的保护器件的顺序是：ESD(TVS管)、隔离变压器、共模电感、电容、电阻，对于原理图缺失上面任意器件顺延布局；严格按照原理图的顺序（要有判断原理图是否正确的能力）进行“一字型”布局。



时钟器件布局：
（1）晶体、晶振和时钟分配器与相关的IC器件要尽量靠近；
（2）时钟电路的滤波器(尽量采用“∏”型滤波)要靠近时钟
电路的电源输入管脚；
（3）晶振和时钟分配器的输出是否串接一个22欧姆的电阻；
（4）时钟分配器没用的输出管脚是否通过电阻接地；
（5）晶体、晶振和时钟分配器的布局要注意远离大功率的
元器件、散热器等发热的器件；
（6）晶振距离板边和接口器件是否大于1inch。



开关电源布局要紧凑，输入\输出要分开，严格按照原理图的要求进行布局，不要将开关电源的电容随意放置。



**电容滤波半径！！！**

电容和滤波器件 ：
（1）电容务必要靠近电源管脚放置，而且容值越小的电容要越靠近电源管脚；
（2） EMI滤波器要靠近芯片电源的输入口；
（3） 原则上每个电源管脚一个0.1uf的小电容、一个集成电路一个或多个10uf大电容，可以根据具体情况进行增减；



1、 布线优先次序要求
a)  关键信号线优先：电源、摸拟小信号、高速信号、时钟信号和同步信号等关键信号优先。
b)  布线密度优先原则：从单板上连接关系最复杂的器件着手布线。从单板上连线最密集的区域开始布线。
c)  关键信号处理注意事项：尽量为时钟信号、高频信号、敏感信号等关键信号提供专门的布线层，并保证其最小的回路面积。必要时应采取屏蔽和加大安全间距等方法。保证信号质量。
d)  有阻抗控制要求的网络应布置在阻抗控制层上，须避免其信号跨分割。



阻抗突变、信号分割，跨分割

差分线做等长的时候蛇形做小波浪，不要做太大的，为了耦合需要。



找客服要叠层模板，最后一讲





设置规则考虑设计文件中的设计瓶颈处。如有 1mm 的 BGA 芯片，管脚深度较浅的，两行
管脚之间只需要走一根信号线，可设置 6/6mil，管脚深度较深，两行管脚之间需要走 2 根信
号线，则设置为 4/4mil；有 0.65mm 的 BGA 芯片，一般设置为 4/4mil；有 0.5mm 的 BGA
芯片，一般线宽线距最小须设置为 3.5/3.5mil；有 0.4mm 的 BGA 芯片，一般需要做 HDI
设计。一般对于设计瓶颈处，可设置区域规则（设置方法见文章尾部[AD 软件设置
ROOM,ALLEGRO 软件设置区域规则]），局部线宽线距设置小点，PCB 其他地方规则设置
大一些，以便生产，提高生产出来 PCB 合格率。