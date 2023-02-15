# 算法面试题：手写笔记还原
### 题目描述
把设备采集到的汉字书写笔迹坐标数据，还原成一张图片(可以考虑png或者svg)，您可以自由选择任何语言或框架实现还原度算法，在笔迹还原的过程中需要关注几点：
- 笔记的真实还原度
- 笔记的平滑度
- 笔记的粗细变化(可结合点的分布和压力值)
- 笔尖初尖(可结合点的分布和压力值)

附上一张图作为参考标准(第一张图不是我们想要的效果，第二张图是我们想要的最低标准)：

<img width="300" alt="image" src="https://user-images.githubusercontent.com/9147956/218914270-e866f740-cbc2-4132-822d-2491749952f2.png">
<img width="300" alt="image" src="https://user-images.githubusercontent.com/9147956/218247997-b8f2c704-bdd6-4df3-be9b-6814d1501848.png">


### 数据描述
我们会提供数个汉字的笔迹数据供您测试和验证。所有汉字的笔迹数据都保存在`data`目录，每个文件是一个汉字书写的笔迹数据。
汉字的笔迹数据是一个三维数组
```
[
  [
    [x坐标,y坐标,书写时压力值],
    [x坐标,y坐标,书写时压力值],
    [x坐标,y坐标,书写时压力值],
    ...
  ],
  [
    [x坐标,y坐标,书写时压力值],
    [x坐标,y坐标,书写时压力值],
    [x坐标,y坐标,书写时压力值],
    ...
  ],
  [
    [x坐标,y坐标,书写时压力值],
    [x坐标,y坐标,书写时压力值],
    [x坐标,y坐标,书写时压力值],
    ...
  ],
  ...
]

```
![image](https://user-images.githubusercontent.com/9147956/217541080-57ad8431-a65d-4198-9173-9141362f16b5.png)

