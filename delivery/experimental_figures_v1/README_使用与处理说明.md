# 实验图件：TEM/HRTEM 与元素 mapping

本版只对作者上传的实验图进行非生成式测量、标注、裁剪、显示增强和排版，没有新增颗粒、晶格条纹或元素色点，也没有将色点随机化或人为均匀化。

## 文件

- `Figure_TEM_HRTEM.png/.tiff`：三联图，2448×824 像素，300 dpi 元数据。
- `Figure_Mapping_display_enhanced.png/.tiff`：显示增强的六联图，2448×1756 像素，300 dpi 元数据。元素名称置于图外黑色边栏，不遮挡信号。
- `Figure_Mapping_original.png/.tiff`：同布局的原始配色/原始强度对照图。
- `individual/`：单个面板及原始/增强 mapping 裁切图。
- SVG为可移动的嵌入图像面板布局，科学影像及标注仍为栅格，并非原生矢量实验数据。
- `Processing_and_measurements.json`：源文件校验值、标尺、测量区域、算法和信号位置核查记录。

## TEM 图及晶格间距

(a)来自1.0007.tiff，保留原50 nm标尺。虚线框对应(b)的裁剪区域。(b)由(a)原图坐标(335,500)至(575,740)裁剪放大，10 nm标尺依据原50 nm/175像素校准后计算，未生成新细节。

(c)来自另一张1.0006.tiff，保留原5 nm标尺。它不是(a)/(b)同一颗粒的逐级放大。右下插图为(c)框选区域的原像素放大。晶格标注依据本图标尺和局部FFT得到：颗粒内部约0.186 nm，外层条纹约0.343 nm，在图中保守标为d≈0.19 nm和d≈0.34 nm。没有直接套用参考图的0.22 nm/0.35 nm，没有未经核实地指定(111)/(002)晶面或合金相。

校准依据嵌入式标尺：5 nm对应144像素，50 nm对应175像素。标尺端点有约1像素的判读歧义，原始仪器nm/pixel元数据仍应核对。测量采用局部平面去趋势、Hann窗和零填充FFT；这些操作只用于分析，没有用于改变最终显微图。多个ROI彼此重叠，不是独立实验重复，也不是统计置信区间。

## Mapping 的处理与限制

报告提供Electron image及Ni、Co、Fe、Cu、Al图。按参考版式排列为Electron image/Fe/Co与Ni/Cu/Al；没有提供Mn，未补造Mn图。未确认采集模式，因此灰度图没有擅自标为HAADF。

增强版用统一gamma=0.65的单调显示变换，并将Fe/Co/Ni/Cu/Al分别显示为黄/青/紫/绿/红。它使已有弱信号更可见，不改变任何源像素上的有/无信号状态。五张源尺寸处理图增强前后的非零信号像素位置逐一核对完全一致，组合图文字放在数据区域外，不遮挡色点。图中稀疏Cu/Al仍保持稀疏，不代表均匀性已由修图证明；不能凭增强图的视觉亮度横向定量元素含量。

所有mapping使用最近邻显示放大，没有插入新的空间信号。颜色和亮度变换仅是对Word报告栅格截图的显示处理，不是重新处理EDS原始计数、谱峰或背景。原图中已有噪声也会保留，不能把增强后噪声当作可信的微量元素分布。原始配色对照版同时提供。

mapping报告缺少空间标尺与像素校准，故本版不套用参考图的50 nm标尺。Cu是否来自样品、铜网或载台仍需作者核实。

## 关于高清晰度

PNG和LZW压缩TIFF为无损输出。原始两张TEM为768×768像素；Word中的mapping有效区域约203×202像素，灰度图约325×324像素。高分辨率画布、300 dpi元数据和显示放大不能恢复原图没有的细节。(b)局部放大及mapping清晰度受这些源像素限制。如需严格的投稿级原始分辨率及标尺，应提供仪器直接导出的高分辨率TIFF、DM3/DM4或EDS原始文件。

## 建议图注

**TEM/HRTEM:** (a) TEM image of the supplied sample. (b) Magnified crop of the boxed region in (a). (c) HRTEM image from a separate supplied field, with an enlarged particle-interior inset. Approximate local fringe spacings are 0.19 nm in the particle interior and 0.34 nm in the outer layered region, estimated using the embedded scale bar and local Fourier analysis. Phase and Miller-index assignments are not made here. Scale bars: (a) 50 nm, (b) 10 nm and (c) 5 nm.

**Mapping:** Electron image and Fe, Co, Ni, Cu and Al elemental-map displays extracted from the supplied EDS report. A shared monotonic gamma display transform (gamma=0.65) and standardized display colors are used in the enhanced version. Original signal positions are retained; no points are added or redistributed. The original-display comparison is supplied. A spatial scale is not assigned because map calibration was not included; the origin of the Cu signal and electron-image acquisition mode require confirmation.
