# Origin 2018b I–V 绘图脚本

五条压力曲线为 0、20、40、50、60 kPa。脚本使用传统 LabTalk 和 Origin 内置 plotxy，不需要 Python、originpro 或第三方插件。数据内置于脚本，电压 -2 至 +2 V，步长 0.2 V，每条 21 点。

## 推荐运行方法

1. 下载并解压整个 ZIP 到一个普通本地目录，例如 C:\Origin_IV。
2. 在 Origin 2018b 中打开 Window（窗口）→ Script Window（脚本窗口）。
3. 输入以下一行，将路径改成实际保存位置，然后按 Enter：

```text
run.section("C:\Origin_IV\IV_Origin2018b.ogs", Main);
```

默认 Main 段使用图片估读后的插值值。如果需要已明确标注的模拟散点图，运行：

```text
run.section("C:\Origin_IV\IV_Origin2018b.ogs", Simulated);
```

每次执行都会新建工作簿和图窗口，不删除旧数据，不覆盖现有工程，也不自动写入本地文件。

## 不想填写文件路径

用记事本打开 Plot_INTERPOLATED.txt，复制全部内容，在 Origin 的 Script Window 中粘贴。选中粘贴的全部脚本，按 Enter 执行。不要把 OGS 文件里的 [Main] 或 [Simulated] 段标题一并当作普通命令粘贴。模拟版使用 Plot_SIMULATED_NOT_MEASURED.txt。

## 图形设置

- 横轴：Voltage (V)，纵轴：Current (mA)。A 列为 X，B–F 列为 Y。
- 轴标题、刻度文字、图例、数据性质标识：Arial，28 pt。
- 五条曲线依次为灰色圆点、蓝色方块、绿色三角、红色菱形、紫色星形，使用连线加标记，标记大小 9 pt。连线宽度沿用 Origin 内置 Line+Symbol 模板默认值。
- X 显示范围 -2.2 至 +2.2 V，Y 范围 -2 至 +2 mA。坐标轴主刻度间隔 1。
- 图例放在左上，图层留出较大页边距以容纳 28 号文字。

## 数据性质与验证

插值版恢复图片曲线趋势，并非每 0.2 V 新测量一次。模拟版是在插值点上加入已声明的小幅演示噪声，不是实验测量、重复测量或误差评估。它保留 SIMULATED / NOT MEASURED 标识。

已静态核对脚本内全部电压和电流数组，与此前提供的 CSV 一致。当前云环境为 Linux，没有 Origin 2018b，因此没有实际运行 Origin、验证其渲染，也没有生成原生 OPJU 文件。若执行时有 LabTalk 报错，请保留完整报错和提示行，便于逐项核对该版本命令。

在 Origin 运行成功后，可以 File → Save Project 保存可编辑工程；高清导出可使用 File → Export Graphs 中的导出对话框，选择 PNG/TIFF 与 600 dpi。保存位置由你选择，脚本不自动覆盖文件。
