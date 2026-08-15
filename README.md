# ICEops Update Repository

> Official ICEops installer, release package, and automatic update repository.

## Recommended System Configuration / 시스템 권장사양

| Component | Recommended |
|---|---|
| OS | Windows 11 64-bit |
| CPU | Intel Core Ultra 7 class or equivalent |
| Memory | 32 GB RAM |
| Storage | NVMe SSD with at least 20 GB free space |
| Network | 1 GbE wired Ethernet recommended for commissioning and high-rate polling |
| Display | 1920×1080 minimum, 2560×1440 recommended |
| Reference platform | ASUS NUC 15 Pro class or equivalent |

### Local AI Assistance

ICEops can use a separately configured local AI server or run local AI models on the same workstation.

- **Fast mode (8B):** 32 GB system RAM recommended.
- **Expert mode (14B):** dedicated NVIDIA GPU recommended for practical response speed.
- **GPU memory:** 8 GB VRAM or more recommended for local GPU-assisted inference.
- CPU-only inference is possible depending on the AI server configuration, but response time can be significantly slower.
- For continuous high-rate polling, HMI visualization, database history, and local 14B AI inference on the same PC, an RTX-class GPU system is recommended.

> Actual resource usage depends on active ports, polling interval, visualization workload, database history, and AI model configuration. For field commissioning, wired Ethernet is recommended even when Wi-Fi or VPN access is also available.

## 한국어

이 저장소는 ICEops 공식 설치 파일 및 자동 업데이트 배포 저장소입니다.

- 최신 설치 파일은 **Releases**에서 다운로드해 주세요.
- 이 저장소에 게시된 공식 설치 파일만 사용해 주세요.
- 자동 업데이트는 설치 전에 SHA-256 무결성 검증을 수행합니다.
- 이 저장소에는 배포 파일만 포함되며 소스 코드는 제공되지 않습니다.
- 권장 시스템은 Windows 11 64-bit, 32 GB RAM, NVMe SSD, 1 GbE 유선 네트워크이며 ASUS NUC 15 Pro급 이상의 시스템을 권장합니다.
- 로컬 AI Expert 14B를 동일 PC에서 사용할 경우 실용적인 응답속도를 위해 NVIDIA RTX급 GPU를 권장합니다.

## English

This is the official download and automatic update repository for ICEops.

- Download the latest installer from **Releases**.
- Use only installers published in this repository.
- Automatic updates verify the installer with SHA-256 before installation.
- This repository contains deployment files only. Source code is not distributed here.
- A Windows 11 64-bit system with 32 GB RAM, NVMe SSD, 1 GbE wired networking, and ASUS NUC 15 Pro-class hardware or better is recommended.
- When running local Expert 14B AI on the same PC, an NVIDIA RTX-class GPU is recommended for practical response speed.

## Deutsch

Dieses Repository ist das offizielle Download- und automatische Update-Repository für ICEops.

- Laden Sie das neueste Installationsprogramm unter **Releases** herunter.
- Verwenden Sie ausschließlich Installationsprogramme, die in diesem Repository veröffentlicht wurden.
- Automatische Updates überprüfen das Installationsprogramm vor der Installation mit SHA-256.
- Dieses Repository enthält ausschließlich Bereitstellungsdateien. Der Quellcode wird hier nicht veröffentlicht.
- Empfohlen werden Windows 11 64-Bit, 32 GB RAM, eine NVMe-SSD, kabelgebundenes 1-GbE-Netzwerk und Hardware der Klasse ASUS NUC 15 Pro oder besser.
- Für den lokalen Expert-14B-KI-Betrieb auf demselben PC wird für praxisgerechte Antwortzeiten eine NVIDIA-RTX-GPU empfohlen.

## 日本語

このリポジトリは、ICEops の公式インストーラーおよび自動アップデート配布用リポジトリです。

- 最新のインストーラーは **Releases** からダウンロードしてください。
- このリポジトリで公開された公式インストーラーのみを使用してください。
- 自動アップデートでは、インストール前に SHA-256 による整合性確認を行います。
- このリポジトリには配布ファイルのみが含まれ、ソースコードは公開されません。
- Windows 11 64-bit、32 GB RAM、NVMe SSD、1 GbE 有線ネットワーク、および ASUS NUC 15 Pro クラス以上のシステムを推奨します。
- 同一PCでローカル Expert 14B AI を使用する場合は、実用的な応答速度のため NVIDIA RTX クラスの GPU を推奨します。

## 中文

本仓库是 ICEops 官方安装程序及自动更新发布仓库。

- 请从 **Releases** 下载最新安装程序。
- 请仅使用本仓库发布的官方安装程序。
- 自动更新会在安装前通过 SHA-256 验证文件完整性。
- 本仓库仅包含发布文件，不提供源代码。
- 推荐使用 Windows 11 64 位、32 GB RAM、NVMe SSD、1 GbE 有线网络以及 ASUS NUC 15 Pro 级别或更高配置的系统。
- 如果在同一台电脑上运行本地 Expert 14B AI，为获得实用的响应速度，建议使用 NVIDIA RTX 级 GPU。

## Español

Este es el repositorio oficial de descarga y actualización automática de ICEops.

- Descargue el instalador más reciente desde **Releases**.
- Utilice únicamente los instaladores publicados en este repositorio.
- Las actualizaciones automáticas verifican el instalador mediante SHA-256 antes de la instalación.
- Este repositorio contiene únicamente archivos de distribución. El código fuente no se publica aquí.
- Se recomienda Windows 11 de 64 bits, 32 GB de RAM, SSD NVMe, red Ethernet cableada de 1 GbE y hardware de clase ASUS NUC 15 Pro o superior.
- Para ejecutar AI Expert 14B localmente en el mismo PC, se recomienda una GPU NVIDIA de clase RTX para obtener tiempos de respuesta prácticos.

## Repository contents

- Release installers
- SHA-256 checksum files
- `update.json` update metadata

ICEops source code, signing keys, license tools, and private build assets are not stored here.
