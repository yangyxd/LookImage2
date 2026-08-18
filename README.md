# LookImage2 - 轻量级专业图像查看器

一款使用 Rust 语言开发的高性能、超轻量图像查看器，专注于提供流畅的图像浏览体验和广泛的格式支持。

#### 欢迎大家使用，有任何建议、问题，可以在此提 Issues！

QQ交流群：793870787
官方网站：
https://yangyxd.github.io/LookImage2/web/
https://lookimage2.pages.dev/

## ✨ 功能特性

### 核心功能
- **多格式支持**：100+ 种图像格式，含 RAW 相机格式、HEIC/AVIF、PSD、EXR、DDS、SVG 矢量、DICOM 医学图像等
- **高性能渲染**：DXGI GPU 硬件加速、抗锯齿、瓦片化大图、SVG 矢量无损缩放、RAW 磁盘缓存，超大图像流畅缩放
- **智能缩放**：支持多种缩放模式（自适应宽度/高度/窗口、1:1、自定义缩放）
- **图像操作**：旋转（90° 步进）、水平/垂直镜像、JPEG 真·无损旋转（MCU 级，画质零损失）、区域裁剪
- **动画支持**：完美支持 GIF、WebP、APNG 等动态图像格式
- **深色模式**：支持明暗主题切换
- **多语言支持**：内置中英文，可通过 res\lang\语言文件.json 扩展

### 用户体验
- **幻灯片播放**：可调间隔、随机、循环、全屏淡出过渡、后台预加载
- **EXIF / 元数据面板**：相机参数、GPS、RGB 直方图、拍摄时间
- **键盘快捷键**：全面的快捷键支持，提升操作效率（设置页可查看）
- **图像编辑**：区域裁剪（三分线辅助、保存/复制/应用视图）
- **文件管理**：目录图像序列浏览（含子目录扫描）、重命名、复制/拖出文件、回收站删除、系统属性对话框
- **文件关联**：设置面板内分组关联管理器，可一键关联/取消
- **手动更新**：设置页可手动检查更新、前往下载（无自动升级）
- **拖拽支持**：支持拖拽图像文件直接打开
- **剪贴板支持**：复制图像（原图/缩放/可视区域）、复制路径/文件名/分辨率

![](https://gitee.com/yangyxd/look-image-bin/raw/master/imgs/001.png)
![](https://gitee.com/yangyxd/look-image-bin/raw/master/imgs/002.png)
![](https://gitee.com/yangyxd/look-image-bin/raw/master/imgs/003.png)

## 📷 支持的图像格式

> 共 100+ 扩展名，以下为常用代表；RAW 共 33 种相机格式，列示主要厂商。

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

### RAW 相机格式（共 33 种）
| 扩展名 | 说明 |
|--------|------|
| `.cr2`, `.cr3` | Canon RAW |
| `.dng` | Adobe DNG |
| `.nef` | Nikon RAW |
| `.arw` | Sony RAW |
| `.rw2` | Panasonic RAW |
| `.orf` | Olympus RAW |
| `.raf` | Fujifilm RAW |
| …（另含 Pentax/Samsung/Leica/Phase One/Hasselblad 等） | 完整 33 种 |

### HEIF / AVIF 格式
| 扩展名 | 说明 |
|--------|------|
| `.heic`, `.heif` | HEIF 容器格式 |
| `.avci`, `.heics`, `.heifs` | HEIF 变体 |
| `.avif` | AVIF 格式（基于 AV1，由内置 libavif + dav1d 解码） |

### 特殊格式
| 扩展名 | 说明 |
|--------|------|
| `.hdp`, `.jxr`, `.wdp` | JPEG XR 格式 |
| `.dcm` | DICOM 医学图像（自研解码器，设置中默认关闭，按需开启） |
| `.eps` | Encapsulated PostScript |
| `.wmf`, `.emf` | Windows 图元文件 |
| `.vst`, `.msk`, `.psp` | 专业绘图软件格式 |
| `.pal` | 调色板格式：Windows RIFF PAL / Dr.Halo / NES / 16-bit PAL |

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

Apache 2.0 License

---

**LookImage2** - 让图像查看更简单、更快、更专业