<img width="468" height="35" alt="image" src="https://github.com/user-attachments/assets/d18480a8-3091-48b4-86f7-d955e6d5fffa" /># TCP 擁塞控制演算法動態視覺化模擬器

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[English Version](README.md)

## 專案簡介
本專案是一個基於 HTML5 Canvas 與 JavaScript 開發的 TCP 擁塞控制演算法模擬器。我們旨在將抽象的網路協議（如 Tahoe, Reno, CUBIC, BBR）轉譯為視覺化的數列動態演進，幫助研究者與學生深入理解擁塞窗口（CWND）的變化規律與級數求和理論。

## 視覺化與理論
模擬器核心遵循 **分段動態遞迴函數** 邏輯：
* **慢啟動 (Slow Start)**：採用等比數列遞迴 ($CWND_{n+1} = CWND_n \cdot 2$)。
* **擁塞避免 (Congestion Avoidance)**：採用等差數列遞迴 ($CWND_{n+1} = CWND_n + 1$)。
* **CUBIC 模型**：利用三次多項式拐點維持高位試探。
* **BBR 模型**：鎖定克萊因羅克交點（Kleinrock Limit）實現恆定速率。

## 使用說明
1. 點擊 [Live Demo](https://leotks0930.github.io/tcp-congestion-control-visualizer/tcp.html) 開啟頁面。
2. 在面板調整 `Loss Ceiling` (擁塞天花板) 與 `Drop Rate` (丟包率)。
3. 點擊 `Start Simulation` 觀察折線圖與影像渲染速度。

## 專案貢獻
* **ltks0930**：核心架構設計與演算法實現、視覺化界面排版與數據圖表製作、數學理論推導與數據分析、技術報告撰寫與背景文獻調研

## 授權聲明
本專案採用 MIT License 開源協議。
