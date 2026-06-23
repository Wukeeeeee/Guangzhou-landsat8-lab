# 广州 Landsat 8 国土类型遥感监督分类实验

这是一个 GIS / 遥感实训项目归档，主要记录基于 Landsat 8 影像的广州市国土类型监督分类流程。

本实验主要在 ENVI 中完成，内容包括影像预处理、研究区裁剪、ROI 样本选取、监督分类与结果记录。当前成果用于课程实训和个人学习记录，不作为正式生产级土地覆盖制图成果。

## 实验流程

已完成或已记录的流程包括：

- 打开并检查两景 Landsat 8 影像
- 辐射定标
- FLAASH 大气校正
- 多光谱影像与全色影像融合
- 两景影像无缝镶嵌
- 利用广州市边界裁剪研究区
- ROI 样本选取
- ROI 可分离性检查
- 监督分类实验

已尝试或记录的分类方法：

- 最大似然法
- 神经网络分类
- 支持向量机分类

当前实验使用的地类：

- 水体
- 植被
- 耕地
- 城镇用地
- 裸地

## 仓库内容

主仓库只保留轻量文件，大体积遥感影像和 ENVI 输出文件不直接提交到 Git。

当前主仓库文件：

- `README.md`：项目说明与数据说明
- `.gitignore`：排除大型 ENVI 栅格文件和临时文件

本地工作目录中还可能包含：

- `workflow.md`：实验流程记录
- `guangzhou_landsat8_report.pdf`：阶段性实验报告
- `ScreenShot/`：ENVI 操作截图
- `FinalData/`：本地 ENVI 中间结果和输出文件

这些本地文件主要用于个人归档，不一定全部上传到主仓库。

## Release 数据

大体积数据文件放在 GitHub Releases 中，不放在 main 分支。

| Release | 文件 | 说明 |
| --- | --- | --- |
| [Guangzhou_Shp](https://github.com/Wukeeeeee/Guangzhou-landsat8-lab/releases/tag/Guangzhou_Shp) | `CantonShp.zip` | 广州市行政边界矢量数据，用于研究区裁剪 |
| [Landsats8_Data_122043](https://github.com/Wukeeeeee/Guangzhou-landsat8-lab/releases/tag/Landsats8_Data_122043) | `LC81220432021019LGN00.zip` | Landsat 8 原始影像数据，轨道号 122/043 |
| [Landsats8_Data_122044](https://github.com/Wukeeeeee/Guangzhou-landsat8-lab/releases/tag/Landsats8_Data_122044) | `LC81220442021019LGN00.zip` | Landsat 8 原始影像数据，轨道号 122/044 |

`.dat`、`.hdr`、`.enp`、规则图像和其他 ENVI 中间结果文件体积较大，已通过 `.gitignore` 排除，不直接进入 Git 版本库。

## 说明

本项目更适合作为 GIS 专业课程实训和个人学习记录。当前分类结果仍有明显局限：

- 广州地区地类复杂，城市、郊区、农田和裸地混合明显。
- 城镇用地、耕地、裸地在部分区域光谱特征相近，容易发生混分。
- Landsat 影像空间分辨率有限，难以精细区分城市绿地、林地和小尺度地物。
- 部分分类结果可能存在椒盐噪声，需要进一步后处理和精度评价。

后续可继续补充 ROI 优化、分类后滤波、混淆矩阵精度评价，以及不同分类器结果对比分析。
