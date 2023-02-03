# 轴相关配置

1.打开路径：本地磁盘（C：）\>用户\>Administrator\>AppData\>Roaming\>NDTSCAN

2.打开文件：scanner\_acs

3.修改文件配置

AxisNo,0,1,2,3 轴序号

Enable,True,True,False,True 对应的轴是否可用

Label,Axis00,Axis01,Axis02,Axis03 可以给轴取名字

SpeedLow,10,10,10,10 最低速度

SpeedMid,50,50,50,50 中等速度

SpeedHigh,100,100,100,100 最高速度

SpeedMax,100,100,100,100 最大速度

AccelMax,100,100,100,100 加速度

InitOrder,2,3,0,1 轴初始顺序

HomeOffset,200,200,200,10 走到限位之后，走多少回到原点（除Z轴其他都是先往负的方向走，Z轴向上走）

InitDirection,CCW,CW,CCW,CW cw顺时针 ccw逆时针

PresetOrder, 2,3,0,1 轴移动顺序建议和初始顺序一致（1表示对应的轴第一个移动，2表示第二个，3表示第三个）

PresetSpeed,Mid,Mid,Mid,Mid 移动到点位的速度

Length,400,400,100,100 每个轴的长度

AxisDisc,SCAN,STEP,NONE,FOCUS 线性/Grid托盘扫描时，序号对应轴 0是扫描轴，1是步径 2是焦距对应的其实是X、Y、Z