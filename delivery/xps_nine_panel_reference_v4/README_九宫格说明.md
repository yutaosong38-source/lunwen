# XPS 九宫格文献临时补图版

本版按博士论文第 6 章图 6-4 的九宫格风格排版：a 总谱、b Co 2p、c Fe 2p、d Ni 2p、e Mn 2p 能区、f Cu 2p、g N 1s 能区、h C 1s、i O 1s 能区。博士论文中 V 2p 的位置换成作者要求的 Cu 2p，不把 V 曲线改标为 Cu。Mn、N、O 依作者要求暂用博士论文图，其他六个子图使用 A.xls 数据；所有来源明确分开。

本版按作者指示，以博士论文图 6-4 的 Mn 2p、N 1s、O 1s 三张子图临时补齐九宫格。它是一张混合来源的排版初稿，不是九张属于当前样品的实测谱。a 为 A.xls 总谱；b/c/d/f/h 为 A.xls 的已有高分辨扫描及探索性模型；e/g/i 是论文 CoFeNiMnV/NCNTs-800 样品的文献参考原图，均醒目标注 LITERATURE ONLY / DIFFERENT SAMPLE，投稿前必须替换。

Fe/Co 包含源仪器明确记录的其他金属 Auger 重叠；经验项未被唯一指认为 Fe²⁺/Fe³⁺ 或 Co²⁺/Co³⁺。Ni 氧化相关项仍待参考线形确认。Cu 信号弱，宽损失项边界受限，价态未确认；Cu⁰/Cu⁺ 需 Cu LMM 等额外证据区分。C 主包络两个数值项中心相差约 0.23 eV，在图中合并显示；不是独立 sp²/sp³ 化学态。问号、Oₓ、Sat.、Loss 等都表示暂定候选或包络解释，不报告任何价态百分比。

作者确认 Mo3d Scan 表名误写、认为实际应为 Mn，但原页能量轴仍为 221.4–245.4 eV，不对应 Mn 2p。根据作者后续明确指示，本版 Mn 子图临时引用博士论文中有明确来源的 Mn 2p 图；没有把该错误能区数据改标或转换为 Mn。借用图不证明当前样品的 Mn 价态。

五个高分辨图显示原始测量点、模型总包络加仪器 Smart 背景、各经验项相对背景的填色及蓝色仪器背景。仅为显示，对每张图采用一个统一线性坐标变换；其偏置、比例记录在 Panel_manifest.json。原始结合能和数值 CSV 保持不变。 文献子图仅从 PDF 内嵌原图裁出图内区域，保留原曲线、点、价态/键合标签；不重拟合、不改变峰或编造数值 CSV。三图原始裁剪尺寸约为 350×283 像素，600 dpi 导出不能增加其真实细节；未用 AI 锐化或生成曲线。SVG/PDF 中这三图为内嵌位图，其他五张模型图及总谱为原生矢量图元。

补全要求：同一样品 Mn 2p 约 635–660 eV、N 1s 约 392–408 eV、O 1s 约 526–544 eV 的高分辨原始数据；锰价态确认建议再提供 Mn 3s 及匹配参考谱。要按论文提交最终价态图，还需复核能量校准、背景、多重态和 Auger 参考线形。

## 下载内容

- 主图 PNG/TIFF：7200×7200 像素，600 dpi，TIFF 为 LZW 无损压缩。
- 主图 SVG/PDF：六个数据子图为矢量曲线及文字，三个文献子图为内嵌位图。不是原生 Origin 工程。
- individual：a–i 九个单图的 PNG/SVG，其中三个明确为不同样品的文献参考。
- data：全部原始扫描 CSV、已有拟合曲线 CSV ；不为文献位图编造数值点；可导入 Origin。
- Peak_meanings_reference_v4.docx / Peak_meanings_v3.csv：五种已有高分辨谱的 27 个数值项说明；C 主包络前两项在图中合并。
- Fit_report_v1_context.json、Interpretation_report_v2_context.json、诊断图：数值模型、残差、背景与限制。
- Panel_manifest.json：各图数据来源、线性显示变换、暂定性和缺失高分辨状态。


布局参考：Sibt ul Hassan 博士论文，第 6 章图 6-4，印刷页 134 / PDF 第 145 页。论文样品为 CoFeNiMnV/NCNTs-800，与当前实测数据不能等同。未复制其峰位、价态比例或曲线作为当前样品证据。

## 三个文献子图的标签解释（不能作为当前样品结论）

Mn 2p — Mn²⁺ / Mn³⁺：文献原图将对应峰群标为 Mn²⁺ 和 Mn³⁺；这些是文献样品的报告，不是当前样品的测定。
Mn 2p — Sat.：文献原图标注的卫星项；不代表新增独立价态。
N 1s — Graphitic N：原图的石墨型氮标签；这里只解释名称，不证明当前样品含有该键合环境。
N 1s — Pyrrolic N：原图的吡咯型氮标签；属于文献样品的报告。
N 1s — Pyridinic N：原图的吡啶型氮标签；属于文献样品的报告。
O 1s — C–O / C=O：文献原图标注为 C–O 和 C=O 相关氧；保留原标签，不据此推断当前样品的氧键合态或复核其唯一性。

literature_reference/ 保存论文原始内嵌图和三个原像素裁剪，原始局部约 350×283 像素；数据 CSV 不包含虚构的文献分峰点。

建议图注：Mixed-source XPS layout draft. Panels (a), (b), (c), (d), (f), and (h) are based on A.xls; region decompositions and chemical assignments are exploratory. Panels (e), (g), and (i) are reproduced as explicitly marked literature references from Sibt ul Hassan, Doctoral Thesis, Fig. 6-4 (PDF page 145), for a different sample, CoFeNiMnV/NCNTs-800. These three panels are temporary layout placeholders, not measured spectra of the present sample, and must be replaced before submission. No oxidation-state percentages are inferred.