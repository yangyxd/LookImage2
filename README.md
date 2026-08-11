# LookImage2 - 轻量级专业图像查看器

一款使用 Rust 语言开发的高性能、超轻量图像查看器，专注于提供流畅的图像浏览体验和广泛的格式支持。

#### 欢迎大家使用，有任何建议、问题，可以在此提 Issues！

QQ交流群：793870787
官方网站：https://yangyxd.github.io/LookImage2/web/

## ✨ 功能特性

### 核心功能
- **多格式支持**：支持 50+ 种图像格式，包括 RAW 相机格式
- **高性能渲染**：基于 GPU 的硬件加速渲染，支持超大图像流畅缩放
- **智能缩放**：支持多种缩放模式（自适应、1:1、缩放至窗口等）
- **图像操作**：旋转（90°/180°/270°）、翻转、亮度/对比度调节
- **动画支持**：完美支持 GIF、WebP 等动态图像格式
- **深色模式**：支持明暗主题切换

### 用户体验
- **平滑滚动**：流畅的图像切换体验
- **键盘快捷键**：全面的快捷键支持，提升操作效率
- **文件管理**：支持查看目录中的图像序列，快速切换
- **拖拽支持**：支持拖拽图像文件直接打开
- **剪贴板支持**：支持复制图像到剪贴板

![](https://gitee.com/yangyxd/look-image-bin/raw/master/imgs/001.png)
![](https://gitee.com/yangyxd/look-image-bin/raw/master/imgs/002.png)
![](https://gitee.com/yangyxd/look-image-bin/raw/master/imgs/003.png)

## 📷 支持的图像格式

### 常见格式
| 格式 | 扩展名 | 说明 |
|------|--------|------|
| PNG | `.png` | 无损压缩格式 |
| JPEG | `.jpg`, `.jpeg`, `.jpe`, `.jfif`, `.jfi`, `.jif` | 有损压缩格式 |
| GIF | `.gif` | 动态图像格式 |
| BMP | `.bmp`, `.dib` | 位图格式 |
| WebP | `.webp` | Google 开发的现代格式 |
| TIFF | `.tiff`, `.tif` | 专业图像格式 |
| ICO | `.ico`, `.cur` | 图标格式 |
| SVG | `.svg` | 矢量图形 |
| HDR | `.hdr` | 高动态范围图像 |

### 专业格式
| 格式 | 扩展名 | 说明 |
|------|--------|------|
| JPEG 2000 | `.jp2`, `.jpx`, `.j2k`, `.jp4` | 新一代 JPEG 格式 |
| PSD | `.psd`, `.pdd` | Photoshop 格式 |
| PCX | `.pcx` | 老式位图格式 |
| EXR | `.exr` | 电影级 HDR 格式 |
| QOI | `.qoi` | 快速无损格式 |
| DDS | `.dds` | DirectDraw 表面格式 |
| TGA | `.tga` | Targa 格式 |
| PNM | `.pbm`, `.pgm`, `.ppm`, `.pam` | Netpbm 格式 |

### RAW 相机格式
| 扩展名 | 说明 |
|--------|------|
| `.cr2`, `.cr3` | Canon RAW |
| `.dng` | Adobe DNG |
| `.nef` | Nikon RAW |
| `.arw` | Sony RAW |
| `.rw2` | Panasonic RAW |
| `.orf` | Olympus RAW |
| `.raf` | Fujifilm RAW |

### HEIF / AVIF 格式
| 扩展名 | 说明 |
|--------|------|
| `.heic`, `.heif` | HEIF 容器格式 |
| `.avci`, `.heics`, `.heifs` | HEIF 变体 |
| `.avif` | AVIF 格式（基于 AV1 编码，需额外构建工具） |

### 特殊格式
| 扩展名 | 说明 |
|--------|------|
| `.hdp`, `.jxr`, `.wdp` | JPEG XR 格式 |
| `.dcm` | DICOM 医学图像 |
| `.eps` | Encapsulated PostScript |
| `.wmf`, `.emf` | Windows 图元文件 |
| `.vst`, `.msk`, `.psp` | 专业绘图软件格式 |
| `.pal` | 调色板格式：Windows RIFF PAL / Dr.Halo / NES / 16-bit PAL |

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

### 开发规范
- 使用 Rust 2021 edition
- 代码风格遵循 `rustfmt`
- 提交前运行 `cargo test` 确保测试通过

## 📄 许可证

Apache 2.0 License

---

**LookImage2** - 让图像查看更简单、更快、更专业