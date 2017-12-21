#概述
>该项目的主要功能用来**提醒车辆的保养情况**。从时间、里程等方面制定相应的规则，并进行相应的提醒。

#运行
>1.进入src/company/thoughtworks ，找到Main类。

>2.运行main方法。（建议在eclipse中运行，本人使用jdk版本为1.7 ）

>3.输入测试用例。将下面文字粘贴到控制台，点击回车两次（第一次回车用来作为输入终止的条件），得到相应的结果。

PS：测试用例见官方文档，直接拷贝即可。

#源码文件的结构
## 业务逻辑文件
>为了方便，将所有的业务放到了VehicleMaintenance中（写的比较匆忙，待重构）。

>【**VehicleMaintenance**】负责接受当前日期和车辆的信息。然后根据保养以及报废的规则进行相应的处理。

>【**CarInfo,CarInfoComparator**】在VehicleMaintenance中，有关于car信息的实体（CarInfo），CarInfo 负责存储输入的汽车的基本信息。与CarInfo 相关的是比较器CarInfoComparator，该类的功能是制定对于CarInfo的排序规则，这里按照车辆的车牌号进行排序。

>【**TimeUtils**】提供了一些在VehicleMaintenance 中需要用到的和时间计算相关的内容。

##测试文件
>【**Main**】用于查看整体的运行效果。

>【**src\company\thoughtworks\test**】文件中存储了一些用junit写的测试用例。测试的对象主要为TimeUtils,VehicleMaintenance 中的部分关键函数。

#测试
>【Main方式运行测试】（见：运行章节）

>【单元测试】建议在eclipse下运行，首先需要导入junit包 ，然后分别以单元测试运行的方式运行 src\company\thoughtworks\test 下的 **VehicleMaintenanceTest ， TimeUtilsTest**。

#缺点
>【**封装性**】VehicleMaintenance 的封装性做的并不是很好，很多内部的函数设置成了public,当时主要是为了方便测试，所以选择一种较为粗鲁的方式。

#感谢
>感谢thoughtworks，在coding的过程中，让我加深了很多软件工程方面的理解。
