---
title: '3D打印机维护手册'
date: '2025-08-28T02:50:00+08:00'
cover: "/covers/3DPrinter01.png"
description: 'AEA 3D打印机日常维护手册，包含常见问题解决方法，以及官方维护指南。'
tags: ["3D打印机", "手册", "维护"]
---
如果你不是科协成员，请勿私自维修打印机，若有需要请联系科协管理员。如果你对3D打印感兴趣，想要学习相关操作，欢迎随时与我们联系。

<a href="https://www.bambulab.cn/zh-cn" target="_blank">拓竹官网</a>

<a href="https://wiki.bambulab.com/zh/home" target="_blank">拓竹Wiki</a>

---

科协现有两台拓竹3D打印机，均为FDM（熔融沉积建模）类型的3D打印机。以下是对这两台打印机的日常维护手册，包含常见问题解决方法，以及官方维护指南。

第一台购置于2023年5月8日，型号为拓竹P1P，至今（2025/8/27）已工作1650h，现状态良好。

<img src="/images/3DPrinterMaintenance/printer_p1p.png" style="width:65%;">

第二台购置于2025年5月24日，型号为拓竹P1S，配备AMS自动换料系统。

<div style="display: flex; justify-content: space-between; align-items: center;">
  <figure style="margin: 0 10px;">
    <img src="/images/3DPrinterMaintenance/p1p-footer.png" style="width:95%;">
    <figcaption>打印机 P1P</figcaption>
  </figure>
  <figure style="margin: 0 10px;">
    <img src="/images/3DPrinterMaintenance/p1s-footer.png" style="width:95%;">
    <figcaption>打印机 P1S</figcaption>
  </figure>
</div>

---
## 日常使用

- 1. 由于打印机工作时会产生不同频率振动，不建议将其放在焊接操作台上。

- 2. 每次更换打印机位置时，需要在工况（放好耗材卷或AMS）进行打印机校准。具体方法参照<a href="https://wiki.bambulab.com/zh/general/printer-calibration" target="_blank">打印机校准指南</a>

- 3. PLA耗材在开封后需防潮保存。AMS具有较好密封性，内部有变色硅胶吸湿。更换耗材后请 **及时关闭舱门**。

- <span style="color: red;"> 4. 无论何时，都强烈建议在发布打印工作前检查打印板是否正确放置，是否有残留异物</span>

## 耗材更换

如果你没有看过 <a href="https://wiki.bambulab.com/zh/general/swaping-new-filament-with-bambu-reusable-spool" target="_blank">这里</a>，请在更换耗材前务必查看，即便你是科协理事并且之前更换过耗材。不正确的操作会导致 **耗材卷散开**。

需要注意的点

- 纸卷凹槽对应好料盘凸起
  
- 确认料盘旋转到位
  
- 检查旧料盘标签是否和所更换耗材对应
  
虽然AMS可以自动识别耗材，但P1P的打印仍需手动选择耗材，为避免打印失误，请**务必确认**标签正确，特别是同时购买同种颜色的PLA、 PLA Matte 等耗材时。

<figure>
<img src="/images/3DPrinterMaintenance/9244.jpg" style="width:35%;">
<figcaption>将料盘卡扣咬合到位</figcaption>
</figure>

由于ABS耗材打印时会产生有害气体，并且打印质量较差，故无特殊要求科协不会使用ABS耗材。

打印PLA-CF（含碳纤维）时，请务必使用**硬化钢**喷嘴，否则会对普通喷嘴产生不可逆损坏。

<a href="https://www.bambulab.cn/zh-cn/filament-guide" target="_blank">耗材指南</a>

## 出现了问题？

### 离线打印
目前两台打印机均已连接至科协WiFi。当网络异常时，除连接个人热点打印外，还可使用打印机上的SD卡进行打印。请参考：<a href="https://wiki.bambulab.com/zh/p1/manual/how-to-print-from-sd-card" target="_blank">离线打印</a>

插拔SD卡时请<span style="color: red;">务必关闭打印机电源</span>。

关于离线打印颜色的选择：

- 通过拓竹云服务发送打印任务时，打印机会将切片文件和打印配置保存在 microSD 卡的 cache 文件夹中。通过打印机屏幕再次打印该文件时，打印机会读取保存的打印配置，选择**之前打印**使用的槽位进行打印。

- 使用 Bambu Studio 在局域网模式发送打印任务，并通过屏幕选择该切片文件进行二次打印，打印机会读取切片文件中模型使用的颜色 ID，匹配对应的槽位 ID 进行打印。

- 发送切片文件至打印机或导出至 microSD 卡时，打印机会读取切片文件中模型使用的颜色 ID，匹配对应的槽位 ID 进行打印。


### 关于HMS错误代码
HMS (Health Management System，健康管理系统) 用于指示打印机和AMS的健康状态、打印件质量，并通过提供告警及排故建议帮助用户快速定位及解决问题。当看到HMS提示的消息时，请**尽快处理**，避免影响打印质量。

直接在 <a href="https://wiki.bambulab.com/zh/home" target="_blank">拓竹Wiki</a> 上搜索HMS错误代码即可找到对应的解决方法。

### 打印板粘附力下降
打印板粘附力下降会导致打印失败，解决方法为**清洁打印板**，或添加裙边和支撑，或使用打印胶水。具体请参考<a href="https://wiki.bambulab.com/zh/general/textured-PEI-plate-not-working-as-expected" target="_blank">Bambu Lab纹理PEI打印板质量与预期不符</a>


### 堵头
请参考<a href="https://wiki.bambulab.com/zh/x1/troubleshooting/nozzle-clog" target="_blank">解决方法</a>

### 打印质量问题
关于其他打印质量问题，可参考此链接
<a href="https://wiki.bambulab.com/zh/knowledge-sharing/common-print-quality-problem" target="_blank">常见打印质量问题和解决办法</a>

打印维修过程中，<span style="color: red;">务必切断电源。</span>任何排线的热插拔都可能损坏机器内部芯片，尤其是正面的冷却风扇。
## 其他
竞速小船用于测试打印机 <a href="https://www.3dbenchy.com/download/" target="_blank">竞速小船模型下载</a>
<img src="/images/3DPrinterMaintenance/3DBenchy.png" style="width:50%;">
