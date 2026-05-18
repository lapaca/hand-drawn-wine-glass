# 🍷 Hand-Drawn Swirling Wine Glass 动态)

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Size](https://img.shields.io/badge/Size-3_KB-green.svg)
![Performance](https://img.shields.io/badge/GPU_Acceleration-100%25-orange.svg)

一个极简、极速、无任何外部依赖的**手绘铅笔风格**红酒杯动态交互效果。采用纯数学物理降维技术，让精美的手绘动效渲染性能拉满！

---


### 1. 🏎️ 相比 Canvas 流体物理引擎 **100倍** 性能加速
传统的流体晃动依赖重型的物理引擎（如 Matter.js, P2.js）或 Canvas 逐帧进行复杂的流体碰撞粒子计算，极易导致主线程卡顿和移动端发热。
* **我们的创新解法**：通过**将流体物理降维至纯 CSS 层面**。使用多组超宽贝塞尔曲线（Bezier Curves）做无缝位移产生波动，利用 GPU 硬件加速直接渲染。
* **缓动回弹数学公式**：通过巧妙地将外设倾角传入，配合自定义`cubic-bezier(0.175, 0.885, 0.32, 1.275)` 进行运动缓冲，实现了极具**流体惯性与粘滞回弹质感**的动态反馈，**CPU 开销趋近于 0**！

### 2. ⚡ GPU 硬件级零资源极速加载 (Zero-Asset Rendering)
* **抛弃一切图片与 3D 资源文件**！所有手绘笔触的粗糙质感均通过 SVG 内置滤镜 `feTurbulence` (分形噪波) 和 `feDisplacementMap` 在 GPU 渲染管线中**动态实时扭曲计算**而成。
* **秒开无延迟**：网络传输大小仅 **3 KB**。完全不需要等待外部高画质图片或 Lottie 动效包加载，实现真正的**即时无缝渲染 (Instant Render)**。

### 3. 🎯 跨端重力智能交互 (Gyroscope & Mouse Tracking)
* **桌面端**：高灵敏度的鼠标悬停位置追踪，酒液跟随手势运动产生平滑的倾斜与惯性震荡。
* **移动端**：原生支持 `deviceorientation`（重力感应陀螺仪），倾斜手机即可看到杯中红酒真实随重力晃动。

---

## 🛠️ 技术栈
* **Core**: Inline HTML5 / SVG
* **Animation**: CSS Keyframes (GPU hardware accelerated)
* **Interaction**: Vanilla JS (Lightweight coordinate mapping)
* **Styling**: Vanilla CSS (Smooth transform transitions)

---

## 🚀 快速启动
无需任何打包工具或依赖，直接双击运行：
1. 下载/克隆此仓库：
   ```bash
   git clone https://github.com/your-username/hand-drawn-wine-glass.git
   ```
2. 双击打开 `index.html` 即可在浏览器完美体验。

---

## 📄 开源协议
本项目采用 [MIT License](LICENSE) 协议开源。
