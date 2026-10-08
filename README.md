# Lively-Nature · 灵动自然

> 自然真实风格 Minecraft 光影 · 柔和光照 · 真实色彩 · 植被增强

---

## 项目简介

**Lively-Nature** 是一套基于 Complementary Reimagined r5 代码架构，面向自然风格视觉体验的 Minecraft Java 版光影。

设计理念：

> *"以自然为灵感，用柔和的光线和真实的色彩还原每一个方块的生命力"*

---

## 核心特性

### 光照 & 色彩
- **自然色调映射**：对比度 1.05 · 饱和度 1.15 · 淡色饱和 1.10
- **柔和泛光**：强度 0.08，营造自然辉光氛围
- **真实色彩**：色彩光照模拟，优化 Mac 兼容性
- **时段色温**：清晨暖调（R+），夜晚冷调（B+），雨天柔和降饱和

### 大气 & 环境
- **大气雾**：距离 120m · 强度 0.80，自然深远感
- **星空增强**：高密度星星（3级），夜空格外出彩
- **洞穴光照**：15（柔和探明），保留洞穴氛围的同时提升可见度
- **阴影亮度**：130 环境补光，阴影更通透

### 植被 & 世界
- **植被增强**：动态草/树叶摆动，风感自然
- **云层品质 3**：最高云渲染，体积感丰富
- **真实水面**：波纹 1.5 · PBR 镜面反射 · 动态折射
- **雨天氛围**：RGB 整体降饱和，冷色调雨水质感

### 性能 & 兼容
- **Mac Apple Silicon 专属优化**：色彩光照模拟替代原生彩色光源
- **TAA + FXAA 混合抗锯齿**：平滑画面
- **零依赖** · 开箱即用 · 轻量体积

---

## 关键参数（common.glsl）

| 参数 | 值 | 说明 |
|------|-----|------|
| SHADER_STYLE | 2 | 自然风格 |
| ATM_FOG_MULT | 0.80 | 柔和大气雾 |
| ATM_FOG_DISTANCE | 120 | 雾距适中 |
| NIGHT_STAR_AMOUNT | 3 | 高密度星空 |
| BLOOM_STRENGTH | 0.08 | 柔和泛光 |
| CAVE_LIGHTING | 15 | 柔和洞穴照明 |
| AMBIENT_MULT | 130 | 阴影通透 |
| TM_CONTRAST | 1.05 | 自然对比度 |
| T_SATURATION | 1.15 | 色彩丰富 |
| T_VIBRANCE | 1.10 | 淡色增强 |
| LIGHT_MORNING_R | 1.05 | 清晨暖色调 |
| LIGHT_MORNING_B | 0.95 | 清晨少蓝光 |
| LIGHT_NIGHT_B | 1.20 | 夜晚冷色调 |
| LIGHT_RAIN_R/G | 0.95 | 雨天降红绿 |
| LIGHT_RAIN_B | 1.05 | 雨天偏蓝 |

---

## 快速开始

### 安装

1. 下载 `Lively-Nature-Shader.zip`
2. 放入 `.minecraft/shaderpacks/`（或你的 Fabric 实例目录）
3. 在 Iris / OptiFine 设置中选择 "Lively-Nature-Shader"
4. 搭配资源包获得更佳视觉效果

### 推荐设置

| 设置项 | 推荐值 | 说明 |
|--------|--------|------|
| 视觉风格 | 自然 | 默认风格 |
| 模拟色彩光照 | 真实色彩 | Mac 专属彩色光源替代方案 |
| 实时阴影 | 高 | 4级阴影品质 |
| 云层质量 | 高 | 体积云效果 |
| 细节质量 | 高 | 完整功能体验 |

---

## 开发信息

### 技术栈
- **基础架构**：Complementary Reimagined r5
- **GLSL 版本**：`#version 130`（macOS ARM 兼容）
- **包装格式**：`shaders/` 前缀 zip

### 项目结构

```
Lively-Nature/
├── shader_pack/                  # 光影源码
│   ├── lib/
│   │   ├── common.glsl           # 核心配置（所有可调参数）
│   │   └── ...
│   ├── lang/
│   │   └── en_US.lang            # 设置界面
│   └── shaders.properties        # 设置页面布局
├── output/                       # 宣传素材
├── 效果/                         # 实机截图
└── README.md
```

### macOS 注意事项
- `COLORED_LIGHTING`（彩色光源）在 Mac 上不可用，已用 `COLOR_LIGHT_MODE` 替代
- 打包时必须保持 `shaders/` 目录结构前缀

---

## 许可

GNU General Public License v3.0 · [github.com/Open-code-Studio](https://github.com/Open-code-Studio)

---

**Lively-Nature · 灵动自然** — Lively Studio (「零」影制作组) 出品 — 让自然的光，照进你的世界