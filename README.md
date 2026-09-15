# LookImage2 - 轻量级专业图像查看器

一款使用 Rust 语言开发的高性能、超轻量图像查看器，专注于提供流畅的图像浏览体验和广泛的格式支持。

#### 欢迎大家使用，有任何建议、问题，可以在此提 Issues！

QQ交流群：793870787
官方网站：https://yangyxd.github.io/LookImage2/web/ 
官方网站：https://lookimage2.pages.dev/

## ✨ 功能特性

### 核心功能
- **多格式支持**：100+ 扩展名，含 33 种 RAW、HEIC/AVIF、**JXL**、**QOI**、PSD、EXR、DDS、SVG 矢量、DICOM 医学图像、**PDF/AI 多页文档**、JXR、MPO等
- **高性能渲染**：DXGI GPU 硬件加速、抗锯齿、瓦片化大图（512×512 分片 + 磁盘缓存）、SVG 矢量无损缩放、缩放/工具栏动画插值、RAW 原图磁盘缓存
- **智能缩放**：自适应宽度/高度/窗口、1:1、自定义缩放；长图专用竖向工具栏（顶/上翻屏/下翻屏/底/锁定画布/适应宽）
- **图像操作**：旋转（90° 步进）、水平/垂直镜像、**JPEG 真·无损旋转**（MCU 级，画质零损失）、区域裁剪（三分线辅助、保存/复制/应用视图）、**高质量放大 2x/4x**（Lanczos 插值，仅内存内视图变更、不写盘，超大图有尺寸保护上限）
- **色彩调整**：亮度 / 对比度 / Gamma / 饱和度 / 锐化 5 项实时 LUT 预览（非破坏式，原图不受影响），支持自动调整、按住对比原图、应用/取消
- **另存为**：原始 / 缩放后 / 可视区域 / **压缩图标**四类；有损格式弹质量参数面板；PNG 额外支持**调色板色深（256 / 128 / 64 / 32 / 16 色）+ oxipng 优化**
- **PDF / AI 多页浏览**：页数 >1 时底部出现独立工具栏（首页 / 上一页 / 下一页 / 末页），`Ctrl + 滚轮` 快速翻页，内存页缓存
- **动画支持**：GIF、WebP、APNG 动态图像播放控制
- **深色模式**：明/暗主题切换

### 用户体验
- **幻灯片播放**：可调间隔（默认 3000ms / 下限 1000ms）、随机（Fisher-Yates 洗牌）、循环、全屏淡出过渡、单槽后台预加载下一帧
- **EXIF / 元数据面板**：相机厂商/型号/镜头、拍摄时间、光圈/快门/ISO/焦距、GPS（经纬度/海拔/方向）、RGB 三通道直方图、文件信息（路径/体积/修改时间）
- **键盘快捷键**：全面的快捷键支持（设置页可查看，当前为只读展示）
- **文件管理**：目录图像序列浏览（含子目录扫描）、重命名（`F3` 内联编辑）、复制文件（可粘贴进资源管理器）、回收站删除（`Ctrl+Delete`，可配置永久删除）、系统**属性**对话框
- **文件操作**：**打开方式**、**打印**（`Ctrl+P`）、桌面背景设置（居中/平铺/拉伸）、**锁屏壁纸设置**（Win10+，含恢复默认）
- **自动保存 / 崩溃恢复**：旋转等修改通过临时标记落盘；启动时自动清理上次崩溃残留的孤儿文件
- **拖拽支持**：拖拽图像文件直接打开
- **剪贴板支持**：复制图像（PNG 双格式：原图精度 / 当前缩放 / 可视区域）、复制路径 / 文件名 / 分辨率
- **文件关联**：设置面板内 8 分组关联管理器（COM 注册 + 注册表回退，每扩展名独立图标）
- **手动更新**：设置页可手动检查更新、前往下载（无自动升级、无自动检查）
- **体验细节**：资源管理器文件排序、Toast 提示、加载耗时显示、工具栏自动隐藏、长图顶对齐

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
| `.pdf`, `.ai` | PDF / Adobe Illustrator **多页文档**（zpdf 解码，页数 >1 可翻页浏览） |
| `.hdp`, `.jxr`, `.wdp` | JPEG XR 格式 |
| `.mpo` | MPO 3D 立体图像 |
| `.dcm` | DICOM 医学图像（自研解码器，设置中默认关闭，按需开启） |
| `.eps` | Encapsulated PostScript |
| `.wmf`, `.emf` | Windows 图元文件 |
| `.vst`, `.msk`, `.psp` | 专业绘图软件格式 |
| `.iff`, `.ilbm` | IFF / ILBM 图像 |
| `.xpm` | X PixMap |
| `.sgi`, `.rgb`, `.rgba`, `.bw` | SGI 图像（RGB / RGBA / BW） |
| `.pcd` | Kodak Photo CD |
| `.pal` | 调色板格式：Windows RIFF PAL / Dr.Halo / NES / 16-bit PAL |

## ⚠️ 注意事项

### 内存使用
- 处理超大图像时会自动使用磁盘缓存（临时文件）
- 临时文件位于系统临时目录，程序退出时自动清理

### Windows 7 兼容

**关于硬件加速（d3dcompiler_47.dll）**：

- `d3dcompiler_47.dll` 在 Win7 上默认不存在，且不再静态链接到 exe（已改为运行时动态加载）。
- 程序启动时会检测该 DLL：缺失则自动关闭 DXGI 硬件加速，回退到 softbuffer 纯软件渲染，
  不会出现"丢失 d3dcompiler_47.dll"弹窗。
- 如需启用 GPU 加速与抗锯齿，可将 `d3dcompiler_47.dll`（约 3.5 MB，微软系统组件）放到 exe 同级目录。

### 安全提示
- 不要从不可信来源下载 DLL 文件
- 建议从官方仓库获取完整发行包

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

Apache 2.0 License

---

**LookImage2** - 让图像查看更简单、更快、更专业