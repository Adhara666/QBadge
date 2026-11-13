<p align="center">
  <img src="docs/images/banner.png" alt="QBadge" width="100%">
</p>

<p align="center">
  <a href="README.md"><img src="https://img.shields.io/badge/English-README-blue" alt="English"></a>
  <a href="README.zh-CN.md"><img src="https://img.shields.io/badge/%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-README-2ea44f" alt="简体中文"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Zotero-8%20%7C%209%20%7C%2010-CC2936" alt="Zotero 8-10">
  <img src="https://img.shields.io/badge/version-0.3.5-blue" alt="version 0.3.5">
  <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey" alt="platform">
</p>

# QBadge

在 Zotero 条目列表中显示中科院期刊分区与高校期刊分区标签。

![QBadge 条目列表](docs/images/overview.png)

## 功能

- **两列独立显示**：`QBadge（中科院2025）`、`QBadge（高校分区）`
- **中科院分区**：大类 / 小类 / TOP，1–4 区配色；小类可选、可排序
- **高校分区**（暂只支持地大，以地大为例）：按学科显示 T1–T6，T1–T4 沿用中科院配色，T5/T6 独立配色
- **离线可用**：安装包内置数据，不联网、不上传、不需要 API Key
- **跨平台**：Windows / macOS / Linux

> 高校分区目前仅支持 **中国地质大学（武汉）**。其他高校暂未支持；如果你希望加入自己学校的目录，欢迎在 Issues 中提出，附上学校名称和目录文件。

## 安装

1. 下载最新 `.xpi`：[Releases](../../releases/latest)
2. Zotero → 工具 → 插件 → 齿轮 → Install Plugin From File…
3. 选择 `.xpi`，重启 Zotero
4. 在条目列表**表头右键**，勾选 `QBadge（中科院2025）` 和 `QBadge（高校分区）`

> 新列默认隐藏，必须在表头右键里手动勾选一次。

## 使用

编辑 → 设置 → QBadge：

### 中科院分区

- 显示内容：大类 + 小类 / 仅大类 / 仅小类
- TOP 标签开关与位置
- 大类 / 小类顺序
- 小类按大类筛选
- 小类多选与编号排序（↑ / ↓ / ×）

### 高校分区

- 高校：暂只支持中国地质大学（武汉）
- 学科多选（默认测绘科学与技术、地理科学）
- 编号排序（↑ / ↓ / ×）

## 配色

| 分区 | 颜色 | 色块 |
|:---:|:---:|:---:|
| TOP | `#8E44AD` | ![TOP](docs/images/swatch-top.png) |
| 1区 / 地大 T1 | `#C0392B` | ![1区](docs/images/swatch-q1.png) |
| 2区 / 地大 T2 | `#E67E22` | ![2区](docs/images/swatch-q2.png) |
| 3区 / 地大 T3 | `#F1C40F` | ![3区](docs/images/swatch-q3.png) |
| 4区 / 地大 T4 | `#7F8C8D` | ![4区](docs/images/swatch-q4.png) |
| 地大 T5 | `#2E86C1` | ![T5](docs/images/swatch-t5.png) |
| 地大 T6 | `#85C1E9` | ![T6](docs/images/swatch-t6.png) |

- 中科院 1–4 区与地大 T1–T4 同色；TOP 独立紫色。
- 地大 T5、T6 使用蓝色系。

## 数据说明

| 数据 | 版本 | 覆盖 |
|:---:|:---:|:---:|
| 中科院期刊分区表 | 2025（官方终版） | 21,772 本期刊 |
| 中国地质大学（武汉）期刊分类目录 | 2023 | 9,922 本期刊，38 个学科 |

- 中科院分区表自 2026 年起停止更新，2025 版为最终版。
- 地大目录按学科划分，级别为 T1–T6；一本刊可属于多个学科，不同学科级别可能不同。
- 地大数据无 ISSN，匹配按「ISSN 映射 + 中英文刊名」。
- 未匹配到的期刊显示空白（悬浮可见「未收录」提示）；会议论文不显示。

## 支持更多高校

高校分区目前只内置中国地质大学（武汉）2023 目录，其他学校暂未支持。

如需加入你的学校，请在 Issues 中提供：

- 学校名称
- 目录名称与版本年份
- 目录文件（Excel / PDF 均可）
- 目录的学科划分和级别说明（如 T1–T5、A/B/C）

## 兼容性

- Zotero 8 / 9 / 10（兼容上限预留到 11.*）
- Windows / macOS / Linux
- **不支持 Zotero 7 及更早版本**

## 常见问题

- **装了插件但看不到列？**
  在条目列表表头右键，勾选对应列。

- **某本刊没有标签？**
  可能不在对应目录中；高校分区支持中文刊名匹配，中科院表只覆盖英文期刊。

- **TGRS 为什么中科院小类是 2 区？**
  中科院大类和小类是两套算法；TGRS 大类为地球科学 1 区 Top，遥感小类为 2 区。

- **MDPI 的 Remote Sensing 为什么没有地大地理分区？**
  地大 2023 目录中该刊只在测绘、信息与通信工程、地信、安全等学科，没有地理科学。

- **提示插件未签名？**
  这是本地安装的正常提示，选择继续安装即可。

## 隐私

插件完全离线运行，不收集、不发送任何数据。

## 反馈

请通过 [Issues](../../issues) 反馈问题，附上 Zotero 版本、操作系统和截图。

## 许可证

本插件为闭源软件，仓库仅提供安装包和文档，不包含源代码。

- 允许个人免费使用，以及分享未修改的原始安装包。
- 禁止反编译、修改、二次分发修改版或用于商业用途。
- 分区数据版权归原机构所有，仅供个人科研参考；如权利人提出要求，将移除相关数据。

## 致谢

- 中科院文献情报中心《期刊分区表》
- 中国地质大学（武汉）期刊分类目录
- Zotero 插件社区
