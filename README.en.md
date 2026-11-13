<p align="center">
  <img src="docs/images/banner.png" alt="QBadge" width="100%">
</p>

<p align="center">
  <a href="README.md">简体中文</a> | English
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Zotero-8%20%7C%209%20%7C%2010-CC2936" alt="Zotero 8-10">
  <img src="https://img.shields.io/badge/version-0.4.0-blue" alt="version 0.4.0">
  <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey" alt="platform">
</p>

# QBadge

Show CAS journal quartiles and university journal tiers directly in Zotero's item list.

![QBadge item list](docs/images/overview.png)

## Features

- **Two independent columns**: `QBadge（中科院2025）` and `QBadge（高校分区）`
- **CAS partition**: major category / minor categories / TOP, 1–4 quartile colors; minor categories are selectable and reorderable
- **University partition** (currently CUG only, using CUG as the example): T1–T6 by discipline; T1–T4 use the same colors as CAS, T5/T6 use separate colors
- **Fully offline**: data is bundled; no network, no upload, no API key
- **Cross-platform**: Windows / macOS / Linux

> The university column currently supports **China University of Geosciences (Wuhan)** only. Other universities are not supported yet. If you want your school's catalog added, please open an Issue with the school name and catalog file.

## Installation

1. Download the latest `.xpi`: [Releases](../../releases/latest)
2. Zotero → Tools → Plugins → gear icon → Install Plugin From File…
3. Select the `.xpi` and restart Zotero
4. Right-click the item list header and enable `QBadge（中科院2025）` and `QBadge（高校分区）`

> New columns are hidden by default and must be enabled once from the header context menu.

## Usage

Edit → Settings → QBadge:

### CAS partition

- Display: major + minor / major only / minor only
- TOP tag toggle and position
- Major/minor tag order
- Filter minor categories by major category
- Multi-select and numbered reorder (↑ / ↓ / ×)

### University partition

- University: currently only China University of Geosciences (Wuhan)
- Discipline multi-select (defaults: Surveying and Mapping, Geography)
- Numbered reorder (↑ / ↓ / ×)

## Colors

<table>
  <thead>
    <tr>
      <th align="center" valign="middle">Tier</th>
      <th align="center" valign="middle">Color</th>
      <th align="center" valign="middle">Swatch</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" valign="middle">TOP</td>
      <td align="center" valign="middle">#8E44AD</td>
      <td align="center" valign="middle"><img src="docs/images/swatch-top.png" alt="TOP" width="80" height="24" align="absmiddle"></td>
    </tr>
    <tr>
      <td align="center" valign="middle">CAS Q1 / CUG T1</td>
      <td align="center" valign="middle">#C0392B</td>
      <td align="center" valign="middle"><img src="docs/images/swatch-q1.png" alt="Q1" width="80" height="24" align="absmiddle"></td>
    </tr>
    <tr>
      <td align="center" valign="middle">CAS Q2 / CUG T2</td>
      <td align="center" valign="middle">#E67E22</td>
      <td align="center" valign="middle"><img src="docs/images/swatch-q2.png" alt="Q2" width="80" height="24" align="absmiddle"></td>
    </tr>
    <tr>
      <td align="center" valign="middle">CAS Q3 / CUG T3</td>
      <td align="center" valign="middle">#F1C40F</td>
      <td align="center" valign="middle"><img src="docs/images/swatch-q3.png" alt="Q3" width="80" height="24" align="absmiddle"></td>
    </tr>
    <tr>
      <td align="center" valign="middle">CAS Q4 / CUG T4</td>
      <td align="center" valign="middle">#7F8C8D</td>
      <td align="center" valign="middle"><img src="docs/images/swatch-q4.png" alt="Q4" width="80" height="24" align="absmiddle"></td>
    </tr>
    <tr>
      <td align="center" valign="middle">CUG T5</td>
      <td align="center" valign="middle">#2E86C1</td>
      <td align="center" valign="middle"><img src="docs/images/swatch-t5.png" alt="T5" width="80" height="24" align="absmiddle"></td>
    </tr>
    <tr>
      <td align="center" valign="middle">CUG T6</td>
      <td align="center" valign="middle">#85C1E9</td>
      <td align="center" valign="middle"><img src="docs/images/swatch-t6.png" alt="T6" width="80" height="24" align="absmiddle"></td>
    </tr>
  </tbody>
</table>

- CAS Q1–Q4 and CUG T1–T4 share the same palette; TOP is purple.
- CUG T5 and T6 use blue.

## Data

<table>
  <thead>
    <tr>
      <th align="center" valign="middle">Data</th>
      <th align="center" valign="middle">Version</th>
      <th align="center" valign="middle">Coverage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" valign="middle">CAS Journal Ranking (中科院期刊分区表)</td>
      <td align="center" valign="middle">2025 (final official edition)</td>
      <td align="center" valign="middle">21,772 journals</td>
    </tr>
    <tr>
      <td align="center" valign="middle">CUG journal catalog</td>
      <td align="center" valign="middle">2023</td>
      <td align="center" valign="middle">9,922 journals, 38 disciplines</td>
    </tr>
  </tbody>
</table>

- The CAS table stopped updating in 2026; 2025 is the final edition.
- The CUG catalog is organized by discipline with T1–T6 levels; a journal may belong to multiple disciplines with different levels.
- The CUG catalog has no ISSN; matching uses ISSN mapping plus English/Chinese journal names.
- Unmatched journals are left blank (hover shows "not listed"); conference papers are not displayed.

## More universities

The university column currently bundles only the 2023 CUG catalog. Other schools are not supported yet.

To add your school, open an Issue with:

- School name
- Catalog name and version year
- Catalog file (Excel / PDF)
- Discipline and level definitions (e.g. T1–T5, A/B/C)

## Compatibility

- Zotero 8 / 9 / 10
- Windows / macOS / Linux
- **Zotero 7 and earlier are not supported**

## FAQ

- **The columns don't appear.**<br>
  Right-click the item list header and enable them.

- **A journal has no badges.**<br>
  It may not be in the corresponding catalog. The university column supports Chinese journal names; the CAS table covers English journals only.

- **Why is TGRS a Q2 in the CAS minor category?**<br>
  CAS major and minor categories use different algorithms. TGRS is Q1 Top in Geosciences (major) but Q2 in Remote Sensing (minor).

- **Why does MDPI's Remote Sensing have no CUG Geography tier?**<br>
  In the 2023 CUG catalog, it appears only under Surveying and Mapping, Information and Communication Engineering, Geo-information, and Safety Science — not Geography.

- **Zotero says the plugin is unsigned.**<br>
  This is normal for local installation; continue the installation.

## Privacy

The plugin runs fully offline and does not collect or transmit any data.

## Feedback

Please use [Issues](../../issues) and include your Zotero version, OS, and a screenshot.

## License

QBadge is closed-source software. This repository provides only the installer and documentation; no source code is included.

- Free for personal, non-commercial use; sharing the unmodified original installer is allowed.
- Decompiling, modifying, redistributing modified versions, or commercial use is prohibited.
- Journal classification data belongs to the original institutions and is provided for personal reference only. It will be removed upon a rights holder's request.

## Acknowledgements

- CAS National Science Library journal ranking
- China University of Geosciences (Wuhan) journal catalog
- The Zotero plugin community
