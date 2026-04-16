# Office / Visio 安装与 KMS 激活指南

---

## 一、下载镜像

### Office
```
https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/media/zh-cn/ProPlus2021Retail.img
https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/media/zh-cn/ProPlus2024Retail.img
```

### Visio
```
https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/media/zh-cn/VisioPro2021Retail.img
https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/media/zh-cn/VisioPro2024Retail.img
```

---

## 二、安装镜像

下载完成后，挂载 `.img` 镜像并执行安装程序。

---

## 三、更改 Office License

```bash
cd "C:\Program Files\Microsoft Office\Office*"
```

### Office
```bash
for /f %x in ('dir /b ..\root\Licenses16\ProPlus2021VL_KMS*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"

for /f %x in ('dir /b ..\root\Licenses16\ProPlus2024VL_KMS*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"
```

### Visio
```bash
for /f %x in ('dir /b ..\root\Licenses16\VisioPro2021VL_KMS*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"

for /f %x in ('dir /b ..\root\Licenses16\VisioPro2024VL_KMS*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"
```

---

## 四、KMS 命令激活

```bash
cd "C:\Program Files\Microsoft Office\Office*"

cscript ospp.vbs /inpkey:XJ2XN-FW8RK-P4HMP-DKDBV-GCVGB
cscript ospp.vbs /inpkey:B7TN8-FJ8V3-7QYCP-HQPMV-YY89G

cscript ospp.vbs /sethst:s1.kms.cx
cscript ospp.vbs /act

cscript ospp.vbs /dstatus    # 查看激活状态
```

---

## 五、GVLK 密钥列表

### Office LTSC 2021

| 产品 | Key |
|------|-----|
| Office LTSC 专业增强版 2021 | FXYTK-NJJ8C-GB6DW-3DYQT-6F7TH |
| Office LTSC 标准版 2021 | KDX7X-BNVR8-TXXGX-4Q7Y8-78VT3 |
| Project Professional 2021 | FTNWT-C6WBT-8HMGF-K9PRX-QV9H8 |
| Project Standard 2021 | J2JDC-NJCYY-9RGQ4-YXWMH-T3D4T |
| Visio LTSC Professional 2021 | KNH8D-FGHT4-T8RK3-CTDYJ-K2HT4 |
| Visio LTSC Standard 2021 | MJVNY-BYWPY-CWV6J-2RKRT-4M8QG |
| Access LTSC 2021 | WM8YG-YNGDD-4JHDC-PG3F4-FC4T4 |
| Excel LTSC 2021 | NWG3X-87C9K-TC7YY-BC2G7-G6RVC |
| Outlook LTSC 2021 | C9FM6-3N72F-HFJXB-TM3V9-T86R9 |
| PowerPoint LTSC 2021 | TY7XF-NFRBR-KJ44C-G83KF-GX27K |
| Publisher LTSC 2021 | 2MW9D-N4BXM-9VBPG-Q7W6M-KFBGQ |
| Skype for Business LTSC 2021 | HWCXN-K3WBT-WJBKY-R8BD9-XK29P |
| Word LTSC 2021 | TN8H9-M34D3-Y64V9-TR72V-X79KV |

---

### Office LTSC 2024

| 产品 | Key |
|------|-----|
| Office LTSC Professional Plus 2024 | XJ2XN-FW8RK-P4HMP-DKDBV-GCVGB |
| Office LTSC Standard 2024 | V28N4-JG22K-W66P8-VTMGK-H6HGR |
| Project Professional 2024 | FQQ23-N4YCY-73HQ3-FM9WC-76HF4 |
| Project Standard 2024 | PD3TT-NTHQQ-VC7CY-MFXK3-G87F8 |
| Visio LTSC Professional 2024 | B7TN8-FJ8V3-7QYCP-HQPMV-YY89G |
| Visio LTSC Standard 2024 | JMMVY-XFNQC-KK4HK-9H7R3-WQQTV |
| Access LTSC 2024 | 82FTR-NCHR7-W3944-MGRHM-JMCWD |
| Excel LTSC 2024 | F4DYN-89BP2-WQTWJ-GR8YC-CKGJG |
| Outlook LTSC 2024 | D2F8D-N3Q3B-J28PV-X27HD-RJWB9 |
| PowerPoint LTSC 2024 | CW94N-K6GJH-9CTXY-MG2VC-FYCWP |
| Skype for Business LTSC 2024 | 4NKHF-9HBQF-Q3B6C-7YV34-F64P3 |
| Word LTSC 2024 | MQ84N-7VYDM-FXV7C-6K7CC-VFW9J |

---

## 备注

- 请确保使用合法授权环境。
- KMS 服务器需可访问，否则激活会失败。
- 建议企业环境中使用内部 KMS 服务。

