# Academic-early-warning
大数据可视化课程设计--学生预警

# 设计目的和内容

## **设计背景**

 信息技术高速发展，高校在教育信息化推进的过程中，构建了大量的教育教学以及学工管理的相关学习平台或业务管理系统，随着这些的平台系统的推广使用，累计了大量的数据，将这些数据加以分析和利用，必然能为学校的教学和管理工作带来巨大的帮助。数据挖掘是一门新兴交叉学科，能从海量的、不完整的且有噪声的随机样本数据中训练出分析模型，能快速、有效地挖掘出隐藏在数据里的信息和关系。利用数据挖掘技术提取高校学生数据中潜在的规律和信息，为学校的教育教学改革和学生管理水平的提高提供支持，已经成为当前教育信息化研究的热点。

## **设计目的**

此次课程设计将在前期决策树预测的基础上，选取部分特征属性进行可视化评分与属性之间的关系，对比决策树划分的结果的差异，并分析属性与评分之间的关系，进而得到结论与启发。

# 数据集说明

## **2.1**  **数据集概述**

这些数据是两所葡萄牙中学的学生成绩。数据属性包括学生成绩、人口统计、社会和学校相关特征)，并通过学校报告和问卷收集。两个数据集是关于两个不同科目的表现:数学(mat)和葡萄牙语(por)。在[Cortez和Silva, 2008]中，两个数据集在二元/五级分类和回归任务下建模。其中，目标属性G3与属性G2、G1具有很强的相关性。

## **2.2**  **数据集来源**

数据集来自于kaggle，数据集的名称为Student Grade Prediction，该数据统计了两所葡萄牙学校的中学学生的学习成绩，数据属性包括学生成绩，人口统计学，社会和与学校相关的特征，通过使用学校报告和调查表进行收集。提供了两个关于两个不同学科表现的数据：数学（mat）和葡萄牙语（por），关于数据集的详细介绍可以参照kaggle的官方说明，数据集链接如下：https://www.kaggle.com/datasets/dipam7/student-grade-prediction。

## **2.3**  **数据集特征**

| 数据集特征 | 多元 |
| --- | --- |
| 实例数量 | 649 |
| 性质 | 社会 |
| 属性特征 | 整数 |
| 属性数量 | 33 |

属性特征如下：

1 school-学生的学校(二进制:"GP"-加布里埃尔·佩雷拉或"MS"-穆萨尼奥·达·西尔韦拉)

2 sex-学生性别(二元:"F"代表女性，"M"代表男性)

3 age-学生年龄(数字:从15岁到22岁)

4 address-学生的家庭地址类型(二进制:'U' -城市或'R' -农村)

5 famsize - 家族规模(二进制:'LE3' -小于或等于3或'GT3' -大于3)

6 Pstatus - 父母的同居状态(二进制:"T"--同居，"A"--分居)

7 Medu - 母亲教育(数字:0 -无，1 -小学教育(四年级)，2 â€" 5 - 9年级，3 â€"中等教育或4 â€"高等教育)

8 Fedu - 父亲教育(数字:0 -无，1 -小学教育(4年级)，2 â€" 5 - 9年级，3 â€"中等教育或4 â€"高等教育)

9 Mjob - 母亲的工作(名义上:"教师"、"与保健有关的"、"公务员"(例如行政或警察)、"在家"或"其他")

10 Fjob - 父亲的工作(名义上:"教师"、"与保健有关的"、"公务员"(如行政或警察)、"在家"或"其他")

11 reason - 选择这所学校的理由(名义上:离家近、学校声誉好、课程偏好或其他)

12 guardian - 学生的监护人(名义上:"母亲"、"父亲"或"其他")

13 traveltime - 从家到学校的旅行时间(数字:1 - \<15分钟，2 - 15 - 30分钟，3 - 30分钟到1小时，或4 - \>1小时)

14 studytime - 每周学习时间(数字:1 - \<2小时，2 - 2 - 5小时，3 - 5 - 10小时，或4 - \>10小时)

15 failures - 过去班级失败的次数(数值:如果1\<=n\<3，则为n，否则为4)

16 schoolsup - 额外教育支持(二进制:是或否)

17 famsup - 家庭教育支持(二进制:是或否)

18 paid - 课程科目内的额外付费课程(数学或葡萄牙语)(二进制:是或否)

19 activities - 课外活动(二进制:是或否)

20 nursery - 托儿所(二进制:是或否)

21 higher - 想接受高等教育(二进制:是或否)

22 internet - 在家上网(二进制:是或否)

23 romantic - 有浪漫的关系(二进制:是或否)

24 famrel - 家庭关系质量(数字:1 -非常差到5 -极好)

25 freetime - 放学后的空闲时间(数字:从1 -非常少到5 -非常多)

26 goout - 和朋友出去(数字:从1 -非常低到5 -非常高)

27 Dalc - 工作日酒精消耗量(数字:1 -极低至5 -极高)

28 Walc - 周末饮酒(数字:1 -极低至5 -极高)

29 health - 当前健康状况(数字:从1-非常差到5-非常好)

30 absences - 学校缺勤次数(数字:从0到93)

#这些分数与课程科目相关，数学或葡萄牙语:

G1 -第一阶段等级(数字:从0到20)

G2 -第二阶段等级(数字:从0到20)

32 G3 -最终等级(数字:从0到20，输出目标)

## **2.4**  **程序说明**

操作系统: Microsoft Windows 10 (64 位)

编程语言: Python3.6 编辑器: jupyter notebook

库版本：panda 1.1.5 numpy 1.19.5 matplotlib 2.2.0

# 3参考博客

[1] https://www.jb51.net/article/246009.htm. python决策树预测学生成绩等级实现详情

[2] https://www.jb51.net/article/136567.htm.Python matplotlib绘图可视化知识点整理(小结)

[3] https://blog.csdn.net/qq\_40671063/article/details/127972727. 使用python画柱状图(matplotlib.pyplot)-- 你想要的设置这张图基本都包括

[4]https://blog.csdn.net/wuShiJingZuo/article/details/112791872. 总结了16个常用的matlibplot画图技巧（附源码）
