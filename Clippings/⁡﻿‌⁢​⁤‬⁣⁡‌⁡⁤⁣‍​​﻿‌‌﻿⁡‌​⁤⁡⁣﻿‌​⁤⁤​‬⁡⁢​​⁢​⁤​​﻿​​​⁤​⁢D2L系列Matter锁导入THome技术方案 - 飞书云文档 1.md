---
title: "⁡﻿‌⁢​⁤‬⁣⁡‌⁡⁤⁣‍​​﻿‌‌﻿⁡‌​⁤⁡⁣﻿‌​⁤⁤​‬⁡⁢​​⁢​⁤​​﻿​​​⁤​⁢D2L系列Matter锁导入THome技术方案 - 飞书云文档"
source: "https://tcl-eaglelab.feishu.cn/wiki/N3RrwfyWxixF6BkIZQ0cfbsGnwe?accessToken=ut_k7fjLXvdXgekxYyuubGSaNeWM9gN2vmETo5"
author:
published:
created: 2026-05-13
description:
tags:
  - "clippings"
---
## D2L系列Matter锁导入THome技术方案

李增

徐庆馨

徐亮

王乃稳

曾瑞绅

4月27日修改

正在生成 AI 速览...

本文讨论了 D2L 系列 Matter 锁导入 THome 的技术方案，包括功能概述、技术方案设计和风险评估等内容。关键要点包括：

1.

功能概述：D2 系列锁有校准及设置密码易失败、电量不耐用的问题，计划支持蓝牙近场通信，迭代省电模式、自动落锁等新功能，目标是年内 12 月底产品释放。

2.

技术方案设计 - 设计思路：复用平台导单品逻辑，通过 RN 页面导入控制，部分通用功能采用原生方式迭代开发。

3.

技术方案设计 - 物模型协议：有门锁 - 物模型列表文件，BLE 通讯协议设计原则是让 BLE 端和 MQTT 端在多方面尽量一致，并给出了应用层协议格式和命令定义。

4.

技术方案设计 - 设备配网：加密配网有参考方案，锁校准、管理员密码设置采用后台配置步骤方式，经沟通采用增加字段标识的方案二。

5.

技术方案设计 - 设备控制：明确了设备控制整体流程、连接鉴权流程和设备与 RN 通信协议，还提出了一些待解决的问题和责任人。

6.

技术方案设计 - 自动解锁：具备地理围栏设置功能，包括 Android 地址围栏设置指南、GPS 定位、围栏半径和可选时间等，同时存在一些需要确认的问题。

7.

风险：蓝牙设备碎片化可能导致蓝牙指令下发失败，给出了应对措施，还对各模块任务进行了工时评估，且电子围栏上架可能存在限制。

内容由 AI 生成

<iframe src="https://lf-fb.feishupkg.com/obj/larkdeveloper/app/cli_a3f7707424af9013/current/web_offline/1739190045157_rdmvet84k3s/index.html?uuid=b2da5588e240d3d7544481e851cc8099bd493309&amp;render_times=1&amp;is_online=true" allow="fullscreen *;clipboard-read *;clipboard-write *;local-network-access *;"></iframe>

<table><colgroup><col width="122"> <col width="122"> <col width="122"> <col width="122"> <col width="122"> <col width="122"></colgroup><tbody><tr><td rowspan="1" colspan="1"><p></p><p></p></td><td rowspan="1" colspan="1"><p></p><p></p><p></p></td><td rowspan="1" colspan="1"><p></p><p></p><p></p></td><td rowspan="1" colspan="1"><p></p><p></p><p></p></td><td rowspan="1" colspan="1"><p></p><p></p><p></p></td><td rowspan="1" colspan="1"><p></p><p></p><p></p></td></tr><tr><td rowspan="1" colspan="1"><p></p><p>项目类型</p><p></p></td><td rowspan="1" colspan="1"><p></p><p>平台特性</p><p></p></td><td rowspan="1" colspan="1"><p></p><p>新品类</p><p></p></td><td rowspan="1" colspan="1"><p></p><p>新单品</p><p></p></td><td rowspan="1" colspan="1"><p></p><p>派生单品</p><p></p></td><td rowspan="1" colspan="1"><p></p><p></p><p></p></td></tr></tbody></table>

1.2 背景

D2系列锁上线以来有部分用户反馈：a:在锁setup阶段锁校准及设置管理员密码时容易失败造成不好的用户体验;

b:门锁电量不耐用；因此

1: 支持蓝牙近场通信，提升用户体验;

2:迭代新功能：省电模式、自动落锁；

1.3 需求描述

需求PRD： [https://confluence.tclking.com/pages/viewpage.action?pageId=547223219](https://confluence.tclking.com/pages/viewpage.action?pageId=547223219)

交互PRD： [https://mastergo.com/goto/MSX0Dk6A?page\_id=2:2684&file=166539293360380](https://mastergo.com/goto/MSX0Dk6A?page_id=2:2684&file=166539293360380)

UI设计稿： [https://mastergo.com/file/175518281832637?page\_id=2%3A71&shareId=175518281832637](https://mastergo.com/file/175518281832637?page_id=2%3A71&shareId=175518281832637)

1.4 目标

【待补充】年内12月底产品释放

2.技术方案设计

2.1 设计思路

复用平台导单品逻辑，通过RN页面导入控制，部分通用的其他功能采用原生的方式进行迭代开发

2.2 整体架构

2.3 详细设计

2.3.1 物模型协议

附件不支持打印

<iframe src="https://internal-api-drive-stream.feishu.cn/space/api/box/stream/download/preview_tpl3/?tpl_id=excel&amp;version=4&amp;mount_point=docx_file&amp;updatePreviewTplSeed=1&amp;secbase=https%3A%2F%2Fsecurity.feishu.cn%2Flink%2Fsafety&amp;sl=1&amp;source=docx_file"></iframe>

门锁-物模型列表-hF1YfaSruVlLyxGc.xlsx

评论（0）

跳转至首条评论

0 字

- 上传日志

- 联系客服

- 功能更新

- 帮助中心

- 效率指南

![](chrome-extension://dbjibobgilijgolhjdcbdebjhejelffo/assets/icon.png)