# XPS探索性分峰与图件

本版基于作者上传的A.xls数值谱线及XPS.docx测试说明，绘制Fe 2p、Co 2p、Ni 2p和C 1s四联图。图件采用灰色空心原始数据点、红色总拟合线和彩色组分，结合能从左至右递减。它是可审查的初步数值分解，不是已经确认的价态分析结论。

## 下载文件

- `XPS_deconvolution_4panel.png/.tiff`：4000×3200像素、400 dpi，TIFF为LZW无损压缩。
- `XPS_deconvolution_4panel.svg/.pdf`：矢量曲线和文字，可继续编辑图件；不是原生Origin工程。
- `individual/`：四个单图的PNG和SVG。
- `XPS_fit_diagnostics.png/.pdf`：原始Counts/s、仪器背景、拟合加背景和标准化残差。
- `Peak_parameters.csv`：模型峰位、FWHM、窗口内积分面积及边界限制标记。
- `Model_selection.csv`：候选模型的参数量和加权BIC比较。
- `data/`：未更改的数值谱及逐点背景、总拟合、各组分和残差，CSV可导入Origin。
- `Fit_report.json`：源文件SHA256、假设、参数、拟合诊断和原仪器峰表。

## 能量轴与背景

XPS.docx说明仪器为Thermo K-Alpha，使用最高C 1s峰作284.8 eV参考，并提示碳材料应根据原始VGP/VGD重新核查。A.xls已为这一校准后的参考导出。本版保留导出的能量轴，没有再次平移，也没有用拟合组分中心去重复碳校正。采样步长0.1 eV，精细谱通能50 eV。

扣除A.xls中非零的仪器Smart背景，仅拟合其有效范围。没有把Smart背景误称为重新计算的Shirley或Tougaard背景，没有改写背景列，也没有删掉负的扣背景数据点。

## 模型与限制

拟合使用未平滑的数值数据。Fe/Co/Ni采用非负、有界峰位和峰宽的经验pseudo-Voigt组分，Lorentz混合比例0.3。峰位范围按可见谱线特征选择，并非预先固定为博士论文中的价态峰位。

C 1s先比较单一非对称主峰模型，残差显示其不足。随后比较Voigt包络模型，最终采用五个数值项，其中两个主包络项的中心仅相隔约0.23 eV，在图中合并展示为`P1 + P2`。这两个项**不是分辨出的两种化学态**，不能据此声称sp²/sp³比例、两种价态或两个物种。较高结合能项的化学归属同样未作唯一指定。

候选模型使用加权BIC比较，数值优化使用固定随机种子的多起点搜索。权重由谱边区域相邻差分的MAD噪声估计，再作强度相关缩放；这不是仪器原始计数统计的已验证绝对方差。

局部条件标准误只描述固定背景、固定模型下的优化误差，不包含校准、背景、多重模型和组分相关性的不确定度。CSV中的多位小数是优化结果，不等于实际能量准确度达到0.001 eV。边界受限项与高相关性均须核查。

## 价态归属不能照搬参考图

原仪器峰表明确写有`Fe2p&CoLM2&NiLM45`及`Co2p&FeLM2&NiLM8`，说明Fe、Co区存在其他金属Auger重叠。本版没有把这些重叠项全部强行标成Fe²⁺/Fe³⁺或Co²⁺/Co³⁺。P1、P2等编号表示数值模型组分，不表示独立价态。

本版没有施加经独立参考谱验证的多重态峰群、自旋轨道面积比或Auger参考线形，因此不能作为正式化学态定量模型。Ni及C的组分归属也需要材料和参考线形支持。没有由这些窗口面积计算价态比例、原子百分比或合金的体相组成。

窗口面积单位为Counts/s·eV，是有限拟合区间内的积分。不同元素的面积未经灵敏度因子、传输函数和采样深度校正，不能直接横向比较元素含量。原仪器复合Fe/Co区域的半定量含量也受重叠影响。

## 残差检查

当前四个区域的扣背景R²约为Fe 0.9966、Co 0.9929、Ni 0.9818、C 0.9999。这些数值只说明总包络拟合程度，不能证明分峰唯一或价态归属正确。标准化残差均方仍大于1，局部仍有系统性残差，部分参数到达边界，不能把本版称为已经验证的最终投稿价态拟合。

采用原始VGP/VGD核查背景、充电校正和采集设置，并补充匹配材料的Fe/Co/Ni多重态与Auger参考谱后，才能进一步确认价态和相应峰群面积。无需为追求外观而强迫拟合成参考论文的峰数或峰位。

## 数据范围

四联图按照作者提供的示例选择Fe、Co、Ni、C。A.xls另含Cu 2p、Mo 3d和全谱，原始数值CSV同时保留，但没有纳入本次四联图或编造其价态分峰。Mo区没有明显可靠峰，未据此声称检测到Mo；Cu⁰/Cu⁺通常还需Cu LMM等信息辨别。

建议图注：Exploratory numerical decompositions of the Fe 2p, Co 2p, Ni 2p and C 1s regions, based on the exported binding-energy axis and instrument Smart background. Open circles are unsmoothed background-subtracted data, red curves are model envelopes and colored areas are phenomenological components. The Fe/Co regions contain documented Auger overlaps. Component identifiers are not unique chemical-state assignments; the two C 1s main-envelope terms are unresolved and shown together. Residual diagnostics and numerical component curves are supplied for review.
