共享自行车数据集
==========================================

Hadi Fanaee-T

Laboratory of Artificial Intelligence and Decision Support (LIAAD), University of Porto
INESC Porto, Campus da FEUP
Rua Dr. Roberto Frias, 378
4200 - 465 Porto, Portugal

背景信息
=========================================

自行车共享系统是一种新型的自行车租赁服务，从加入会员到租赁再到还回自行车的整个过程都是自动化的。用户可以通过这些系统轻松地从某个位置租赁自行车并在另一个位置还回自行车。目前，全球有超过 500 个自行车共享项目，并投入了超过 500 万辆自行车。如今，这类系统更是受到大量关注，因为它们可以缓解交通、环境和健康问题。

数据集
=========================================
自行车共享租赁行为与环境和季节之间的关联性很大。例如，天气条件、降水情况、周几、季节、一天的时刻等都会影响到租赁行为。核心数据集采用的是美国华盛顿特区 Capital Bikeshare 系统 2011 至 2012 年的两年间历史记录日志，该数据集可以被公开访问 (http://capitalbikeshare.com/system-data)。按照 2 小时间隔和每日间隔汇总了数据，然后提取并添加了相应的天气和季节性信息。天气信息来自 http://www.freemeteo.com。

相关任务
=========================================

从头开始构建一个神经网络，基于真实的历史数据集对自行车共享情况来进行预测，从而能够调整自行车投放的数量以达到更好的收益。

文件
=========================================

- Readme.txt
- hour.csv - 按照每小时汇总的共享自行车使用人数。记录数：17379 小时
- day.csv - 按照每天汇总的共享自行车使用人数。记录数：731 天

数据集特征
=========================================	
hour.csv 和 day.csv 文件都具有以下字段，但是 day.csv 中没有 hr 字段

- instant：记录索引
- dteday：日期
- season：季节（1：春季，2：夏季，3：秋季，4：冬季）
- yr : 年份（0：2011 年，1：2012 年）
- mnth：月份（1 到12 月）
- hr : 小时（0 到 23 时）
- holiday: 当天是否是假期（数据来自 http://dchr.dc.gov/page/holiday-schedule）
- weekday: 星期几
- workingday: 如果不是周末或假期则是 1 ，否则是 0。
+ weathersit : 
	- 1: 晴朗、飘着几朵云、局部多云
	- 2: 薄雾加多云、薄雾加碎云、薄雾加几朵云、薄雾
	- 3: 小雪、小雨加雷暴加散云、小雨加散云
	- 4: 大雨加冰雹加雷暴加薄雾、下雪加雾
- temp: 标准化温度（摄氏度）。标准化后的值为原数据除以41（最大值）
- atemp: 标准化体感温度（摄氏度）。标准化后的值为原数据除以50（最大值）
- hum: 标准化湿度。标准化后的值为原数据除以100（最大值）
- windspeed: 标准化风速。标准化后的值为原数据除以67（最大值）
- casual: 临时用户数
- registered: 注册用户数
- cnt: 租赁自行车总用户数（包括临时用户和注册用户）

许可
=========================================
在公开场合使用该数据集必须引用以下公开声明：

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}

