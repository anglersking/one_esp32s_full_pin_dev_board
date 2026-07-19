# One ESP32-S3 Full Pin Dev Board

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

ESP32-S3 全引脚引出 40Pin 开发板 —— 集成摄像头、波轮按键、SD 卡、屏幕、扬声器、麦克风、RGB LED，可适配 **小智 AI 直刷**。

---

## 概览

一块把 ESP32-S3 几乎所有可用 GPIO 都引到 40Pin 排针上的开发板，专为需要外设丰富、扩展灵活的场景设计。板载常用外设即插即用，也保留了完整接口供二次开发。

| 特性 | 描述 |
|------|------|
| **主控** | ESP32-S3，双核 Xtensa LX7 @ 240MHz |
| **引脚** | 全 GPIO 引出至 40Pin 2.54mm 排针 |
| **摄像头** | 板载摄像头接口（DVP） |
| **屏幕** | TFT 屏幕接口 |
| **存储** | MicroSD 卡槽 |
| **输入** | 波轮编码器 + 按键 |
| **音频** | 板载扬声器 + 麦克风 |
| **灯光** | RGB LED |
| **兼容** | 支持小智 AI 固件直刷 |

---

## 图片

| 板子整体（正面） | 板子整体（角度） |
|:---:|:---:|
| ![正面](images/1.jpg) | ![角度](images/2.jpg) |

| 布局细节 | 接口区域 |
|:---:|:---:|
| ![布局](images/3.jpg) | ![接口](images/4.jpg) |

| 焊接/成品 | 另一角度 |
|:---:|:---:|
| ![成品](images/5.jpg) | ![另一角度](images/6.jpg) |

---

## 板载资源

### 外设接口

- **摄像头接口** — DVP 并行接口，适配 OV2640 / OV7670 等常见摄像头模组
- **TFT 屏幕接口** — SPI/并行 LCD
- **MicroSD 卡槽** — SPI 模式，存储固件/数据/模型文件
- **波轮编码器** — 旋转编码器 + 按键开关，用于菜单/音量/参数调节
- **扬声器** — 小功率喇叭，I2S 音频 DAC 驱动
- **麦克风** — 板载 MEMS 麦克风，I2S 音频输入
- **RGB LED** — WS2812 / NeoPixel 可寻址彩灯
- **40Pin 排针** — 引出全部可用 GPIO，兼容标准洞洞板/面包板

### 引脚定义

> 详细的引脚映射表将在 PCB 设计文件上传后补充。目前 GPIO 分配遵循 ESP32-S3 标准功能复用，全引脚均以丝印标注在板面。

---

## 软件 / 固件

### 小智 AI 直刷

本开发板专为 **小智 AI**（XiaoZhi）固件设计，固件可直接刷入运行，无需额外硬件修改。

小智固件已默认适配板载所有外设：
- 摄像头画面采集
- 屏幕显示
- 音频输入输出（语音对话）
- 波轮按键交互
- RGB 状态灯效

### 通用 Arduino / ESP-IDF

板载外设驱动兼容 Arduino 和 ESP-IDF 框架，也可作为通用 ESP32-S3 开发板使用。

---

## 参考

- [ESP32-S3 数据手册](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf)
- [小智 AI 项目](https://github.com/78/xiaozhi-esp32)（待核实链接）

---

## 许可

本项目基于 [MIT License](LICENSE) 开源。

Copyright (c) 2026 Wanshan Pang
