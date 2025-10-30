[README.md](https://github.com/user-attachments/files/23222921/README.md)
 振动系统综合模拟器

 2025 VLP 挑战赛参赛作品

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/zh-CN/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript)
[![Canvas API](https://img.shields.io/badge/Canvas_API-4285F4?style=flat&logo=google-chrome&logoColor=white)](https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API)
项目概述

振动系统综合模拟器是一个基于Web技术的交互式物理教学工具，专为物理教育和振动力学学习设计。本项目采用纯前端技术实现，无需任何后端支持或数据库，可在现代浏览器中直接运行。

该模拟器提供了三种经典振动系统的可视化模拟：
- **简谐振动（Simple Harmonic Motion）**
- **阻尼振动（Damped Oscillation）**
- **受迫振动（Forced Oscillation）**

通过实时动画演示、交互式参数调节和多维度数据可视化，帮助学生和教师深入理解振动系统的物理特性和数学规律。

---

重要声明

> **本项目为 2025 VLP 挑战赛参赛作品**
>
> - **开源许可**: 采用 MIT 开源许可证
> - **访问权限**: 本仓库设置为公开访问权限
> - **代码开源**: 完全开源，包含完整的中英文注释和环境配置文件
> - **知识产权**: 所有代码和文档遵循 MIT License，允许自由使用、修改和分发

---

核心功能
 1. 三种振动模式模拟

简谐振动模拟器
- 可调节参数：质量、弹簧常数、初始位置、初始速度
- 实时显示：角频率、频率、周期、振幅、总能量
- 可视化图表：位移-时间图、速度-时间图、能量变化图、相位图
- 物理特性：完整展示简谐振动的能量守恒特性

阻尼振动模拟器
- 可调节参数：质量、弹簧常数、阻尼系数、初始条件
- 阻尼类型判断：欠阻尼、临界阻尼、过阻尼自动识别
- 实时显示：振动频率、周期、阻尼类型
- 可视化图表：位移衰减曲线、速度变化、能量耗散过程

受迫振动模拟器
- 可调节参数：系统参数、外力幅值、外力频率
- 共振分析：固有频率、频率比、稳态振幅、相位差
- 可视化图表：位移响应、速度响应、能量变化、共振曲线
- 物理现象：完整展示共振现象和频率响应特性

2. 交互式参数控制

- 实时调节：所有物理参数支持滑块和数值输入双重控制
- 即时响应：参数修改后立即重新计算和渲染
- 动画控制：播放、暂停、重置、速度调节
- 直观反馈：参数变化对系统行为的影响一目了然

 3. 数据可视化

- Canvas图表：基于HTML5 Canvas API的高性能绘图
- 多维展示：同时展示位移、速度、能量等多个物理量
- 实时更新：动画进行时图表同步更新当前状态
- 清晰标注：坐标轴、单位、图例完整标注

 4. 响应式设计

- 移动端优化：单栏布局，适配手机和平板设备
- **桌面端优化**：三栏布局（参数控制-动画演示-图表分析）
- **自适应布局**：根据屏幕尺寸自动调整界面
- **跨平台兼容**：支持主流浏览器和操作系统

---

## 🚀 快速开始

### 运行环境要求

- **浏览器**：Chrome 60+, Firefox 55+, Safari 12+, Edge 79+
- **必需功能**：HTML5 Canvas API、ES6 JavaScript支持
- **网络要求**：无需网络连接（纯离线应用）
- **额外依赖**：无需安装任何库或框架

### 安装与运行

#### 方法一：直接打开（推荐初学者）

```bash
# 下载项目
git clone https://github.com/WQ050204/VLP.git

# 直接双击 index.html 文件在浏览器中打开
```

#### 方法二：使用本地Web服务器（推荐开发者）

**使用Python**：
```bash
# 进入项目目录
cd VLP

# Python 3.x
python -m http.server 8000

# 访问 http://localhost:8000
```

**使用Node.js**：
```bash
# 全局安装 http-server（仅需一次）
npm install -g http-server

# 启动服务器
http-server -p 8000

# 或使用 npx（无需全局安装）
npx http-server -p 8000

# 访问 http://localhost:8000
```

**使用快速启动脚本**：
```bash
# Windows系统
start.bat

# macOS/Linux系统
chmod +x start.sh
./start.sh
```

---

## 📖 使用说明

### 基本操作流程

1. **选择振动模式**：点击顶部的模拟器切换按钮
2. **调整参数**：使用滑块或输入框设置物理参数
3. **开始模拟**：点击"开始"按钮启动动画
4. **观察现象**：观察弹簧振子的运动和物理量变化
5. **查看图表**：点击"显示图表"查看详细的数据分析

### 物理参数说明

#### 简谐振动参数
- **质量 (m)**: 0.1-5.0 kg，影响振动频率和能量
- **弹簧常数 (k)**: 1-50 N/m，决定系统刚度
- **初始位置 (x₀)**: -3 至 3 m，决定振幅
- **初始速度 (v₀)**: -5 至 5 m/s，影响振幅和相位

#### 阻尼振动参数
- **阻尼系数 (c)**: 0-10 Ns/m，控制能量耗散速率
- **阻尼比 (ζ)**: 自动计算，判断阻尼类型
  - ζ < 1: 欠阻尼（振荡衰减）
  - ζ = 1: 临界阻尼（最快回到平衡）
  - ζ > 1: 过阻尼（缓慢回到平衡）

#### 受迫振动参数
- **外力幅值 (F₀)**: 0-10 N，决定稳态振幅
- **外力频率 (ω)**: 0.1-10 rad/s，控制激励频率
- **频率比 (ω/ω₀)**: 接近1时发生共振

---

## 🔬 物理原理

### 简谐振动

**微分方程**：
```
m(d²x/dt²) + kx = 0
```

**通解**：
```
x(t) = A·cos(ωt + φ)
ω = √(k/m)
E = ½kA²
```

其中：
- A: 振幅
- ω: 角频率
- φ: 初相位
- E: 总机械能（守恒）

### 阻尼振动

**微分方程**：
```
m(d²x/dt²) + c(dx/dt) + kx = 0
```

**欠阻尼解**：
```
x(t) = Ae^(-γt)·cos(ωdt + φ)
ωd = √(ω₀² - γ²)
γ = c/(2m)
```

其中：
- γ: 阻尼系数
- ωd: 阻尼频率
- ω₀: 固有频率

### 受迫振动

**微分方程**：
```
m(d²x/dt²) + c(dx/dt) + kx = F₀cos(ωt)
```

**稳态解**：
```
x(t) = A·cos(ωt - δ)
A = F₀/√[(k-mω²)² + (cω)²]
δ = arctan(cω/(k-mω²))
```

**共振条件**：
```
ω = ω₀ = √(k/m)
```

---

## 📊 技术架构

### 技术栈

- **前端框架**：无框架，纯原生JavaScript
- **UI界面**：HTML5 + CSS3
- **图形渲染**：Canvas API
- **动画引擎**：requestAnimationFrame
- **数学计算**：原生JavaScript Math库
- **数值求解**：欧拉法、龙格-库塔法

### 核心技术特点

1. **纯前端实现**：无需后端、数据库或API调用
2. **零依赖**：不依赖任何第三方JavaScript库
3. **高性能**：使用requestAnimationFrame优化动画性能
4. **模块化设计**：三个独立的模拟器模块
5. **响应式布局**：CSS Grid + Flexbox + Media Queries

### 文件结构

```
VLP/
│
├── index.html              # 主应用文件（包含完整代码）
├── README.md              # 项目说明文档
├── LICENSE                # MIT开源许可证
├── requirements.txt       # 运行环境说明
│
├── ENVIRONMENT.md         # 环境配置详细指南
├── DEPLOYMENT.md          # 部署教程
├── CHANGELOG.md           # 版本更新日志
├── CONTRIBUTING.md        # 贡献指南
│
├── package.json           # NPM配置文件
├── .gitignore            # Git忽略配置
├── netlify.toml          # Netlify部署配置
├── vercel.json           # Vercel部署配置
│
├── start.bat             # Windows启动脚本
├── start.sh              # Unix启动脚本
│
└── .vscode/              # VS Code配置
    ├── extensions.json
    └── settings.json
```

---

## 🌐 浏览器兼容性

| 浏览器 | 最低版本 | 测试状态 | 备注 |
|--------|----------|----------|------|
| Chrome | 60+ | ✅ 完全支持 | 推荐使用 |
| Firefox | 55+ | ✅ 完全支持 | 推荐使用 |
| Safari | 12+ | ✅ 完全支持 | macOS/iOS |
| Edge | 79+ | ✅ 完全支持 | Chromium内核 |
| Opera | 47+ | ✅ 完全支持 | Chromium内核 |
| IE | 任何版本 | ❌ 不支持 | 不支持ES6 |

### 必需的浏览器功能
- HTML5 Canvas API
- ES6+ JavaScript（箭头函数、const/let、模板字符串等）
- CSS3 Grid Layout
- CSS3 Flexbox
- requestAnimationFrame API

---

## 📚 文档说明

### 完整文档列表

- **[README.md](README.md)** - 项目主文档（本文件）
- **[ENVIRONMENT.md](ENVIRONMENT.md)** - 环境配置详细指南
- **[DEPLOYMENT.md](DEPLOYMENT.md)** - 多平台部署教程
- **[CONTRIBUTING.md](CONTRIBUTING.md)** - 贡献指南和代码规范
- **[CHANGELOG.md](CHANGELOG.md)** - 版本历史和更新日志
- **[LICENSE](LICENSE)** - MIT开源许可证全文

### 配置文件说明

- **requirements.txt** - 运行环境依赖说明（本项目无需额外依赖）
- **package.json** - NPM项目配置（用于开发工具）
- **.gitignore** - Git版本控制忽略规则
- **netlify.toml** - Netlify平台部署配置
- **vercel.json** - Vercel平台部署配置

---

## 🎓 教育应用

### 适用场景

1. **课堂教学**：物理教师的演示工具
2. **自主学习**：学生的交互式学习平台
3. **实验预习**：物理实验课前的虚拟实验
4. **概念理解**：抽象物理概念的可视化
5. **参数探索**：通过调节参数理解物理规律

### 教学优势

- **直观展示**：抽象的物理概念具象化
- **交互探索**：学生可自主调整参数观察变化
- **即时反馈**：参数修改立即看到效果
- **零成本**：无需实验器材，浏览器即可使用
- **随时随地**：支持电脑、平板、手机多端访问

### 涵盖知识点

- 简谐运动的基本规律
- 能量守恒定律
- 阻尼振动的三种类型
- 受迫振动和共振现象
- 频率响应特性
- 微分方程数值解法

---

## 🔧 开发指南

### 本地开发环境设置

```bash
# 1. 克隆仓库
git clone https://github.com/WQ050204/VLP.git
cd VLP

# 2. 启动本地服务器（任选其一）
python -m http.server 8000
# 或
npx http-server -p 8000

# 3. 在浏览器中打开
# 访问 http://localhost:8000
```

### 代码结构说明

index.html 文件包含三个主要部分：

1. **HTML结构** (第1-1000行)
   - 页面布局和DOM元素
   - 三个模拟器的独立容器
   - 参数控制面板和图表容器

2. **CSS样式** (第1001-1500行)
   - 响应式布局设计
   - 移动端和桌面端适配
   - 动画过渡效果

3. **JavaScript逻辑** (第1501-3000+行)
   - 三个模拟器对象（simpleSim, dampedSim, forcedSim）
   - 物理计算引擎
   - Canvas绘图函数
   - 事件处理和动画控制

### 修改和扩展

如需修改或扩展功能，建议：

1. **添加新的振动模型**：参考现有模拟器结构
2. **修改物理参数范围**：在参数定义处修改min/max值
3. **调整UI样式**：在CSS部分修改样式规则
4. **优化性能**：减少绘制频率或简化计算

详细的开发指南请参考 [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 🚀 部署指南

本项目支持多种部署方式：

### GitHub Pages（推荐）

```bash
# 1. 确保代码已推送到GitHub
# 2. 进入仓库 Settings → Pages
# 3. Source 选择 main 分支
# 4. 点击 Save

# 访问地址：https://wq050204.github.io/VLP
```

### Netlify

```bash
# 方法1：拖放部署
# 访问 netlify.com，拖放项目文件夹

# 方法2：Git连接
# 连接GitHub仓库，自动部署

# 方法3：CLI部署
npm install -g netlify-cli
netlify deploy --prod
```

### Vercel

```bash
# 安装Vercel CLI
npm install -g vercel

# 登录并部署
vercel
```

详细的部署教程请参考 [DEPLOYMENT.md](DEPLOYMENT.md)

---

## 📄 开源许可

本项目采用 **MIT License** 开源许可证。

### 许可证要点

✅ **允许的使用**
- 商业使用
- 修改
- 分发
- 私人使用

⚠️ **限制**
- 作者不承担责任
- 不提供担保

📋 **要求**
- 必须包含版权声明
- 必须包含许可证副本

完整许可证内容请查看 [LICENSE](LICENSE) 文件。

### 版权声明

```
Copyright (c) 2025 振动系统综合模拟器项目组

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🤝 贡献指南

我们欢迎任何形式的贡献！

### 如何贡献

1. **Fork本仓库**
2. **创建特性分支** (`git checkout -b feature/AmazingFeature`)
3. **提交更改** (`git commit -m 'Add some AmazingFeature'`)
4. **推送到分支** (`git push origin feature/AmazingFeature`)
5. **开启Pull Request**

### 贡献类型

- 🐛 Bug修复
- ✨ 新功能开发
- 📝 文档改进
- 🎨 UI/UX优化
- ⚡ 性能优化
- ✅ 测试用例

详细的贡献指南请参考 [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📞 联系方式

### 项目相关

- **GitHub仓库**: [https://github.com/WQ050204/VLP](https://github.com/WQ050204/VLP)
- **Issue反馈**: [https://github.com/WQ050204/VLP/issues](https://github.com/WQ050204/VLP/issues)
- **在线演示**: [https://wq050204.github.io/VLP](https://wq050204.github.io/VLP)

### 比赛信息

- **比赛名称**: 2025 VLP 挑战赛
- **参赛项目**: 振动系统综合模拟器
- **开源许可**: MIT License
- **仓库状态**: 公开访问

---

## 🎯 未来规划

### v1.1.0 计划功能

- [ ] 添加更多振动模型（双摆、耦合振子）
- [ ] 数据导出功能（CSV、图片）
- [ ] 完整的英文界面
- [ ] 移动端手势控制优化
- [ ] 教学模式和引导教程

### v1.2.0 计划功能

- [ ] 3D可视化
- [ ] 声音模拟
- [ ] 多振子系统
- [ ] 混沌振动
- [ ] 在线协作功能

### 长期愿景

打造成为最专业、最易用的物理振动教学平台，服务于全球的物理教育工作者和学习者。

---

## 🙏 致谢

### 感谢以下资源和支持

- **2025 VLP 挑战赛组委会** - 提供展示平台
- **物理教育工作者** - 提供专业建议
- **开源社区** - 提供技术支持
- **MDN Web Docs** - 提供技术文档
- **所有贡献者和使用者** - 持续的反馈和支持

### 技术参考

- Canvas API Documentation - Mozilla Developer Network
- Physics Simulation Techniques - Khan Academy
- Numerical Methods for Differential Equations
- Responsive Web Design Principles

---

## 📊 项目统计

- **代码行数**: ~3000+ 行
- **文件数量**: 19 个文件
- **支持语言**: 中文、英文
- **浏览器支持**: 5+ 主流浏览器
- **响应式断点**: 3 个（移动端、平板、桌面）
- **物理模型**: 3 种振动系统
- **可视化图表**: 10+ 种图表类型

---

## 📝 更新日志

### [1.0.0] - 2025-10-30

#### 新增
- ✨ 简谐振动模拟器
- ✨ 阻尼振动模拟器
- ✨ 受迫振动模拟器
- 📊 实时数据可视化
- 🎨 响应式用户界面
- 📱 移动端和桌面端适配
- 📚 完整的项目文档

详细的更新历史请查看 [CHANGELOG.md](CHANGELOG.md)

---

## ❓ 常见问题

### Q: 为什么动画在某些浏览器上卡顿？
A: 建议使用Chrome或Firefox最新版本，关闭其他标签页以释放资源。

### Q: 可以在手机上使用吗？
A: 可以！本项目完全支持移动端浏览器。

### Q: 如何导出模拟数据？
A: 当前版本暂不支持数据导出，该功能计划在v1.1.0版本中添加。

### Q: 可以添加自定义的振动模型吗？
A: 可以！请参考代码中的模拟器结构，或提交Feature Request。

### Q: 项目是否可以用于商业用途？
A: 可以！本项目采用MIT License，允许商业使用。

更多问题请提交 [Issue](https://github.com/WQ050204/VLP/issues)

---

## 🔗 相关链接

- **项目主页**: [GitHub Repository](https://github.com/WQ050204/VLP)
- **在线演示**: [GitHub Pages](https://wq050204.github.io/VLP)
- **问题反馈**: [Issues](https://github.com/WQ050204/VLP/issues)
- **技术文档**: [Wiki](https://github.com/WQ050204/VLP/wiki)
- **Canvas API**: [MDN文档](https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API)
- **物理教程**: [Khan Academy](https://www.khanacademy.org/science/physics)

---

## 📌 关键词

`物理模拟` `振动系统` `简谐运动` `阻尼振动` `受迫振动` `共振` `Canvas` `JavaScript` `HTML5` `教育工具` `交互式学习` `可视化` `开源项目` `MIT License` `2025 VLP`

---

<div align="center">

**© 2025 振动系统综合模拟器项目组**

**2025 VLP 挑战赛参赛作品**

**MIT License | 开源 | 免费使用**

---

**如果这个项目对您有帮助，请给我们一个 ⭐ Star！**

**[⬆ 回到顶部](#振动系统综合模拟器)**

</div>
