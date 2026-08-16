# ICEops Update Repository

> Official ICEops installer, release package, and automatic update repository.

## ⚠️ REQUIRED: Master Network & IODD Initialization

**Use the local network for the Master and keep Internet access available for IODD synchronization.**

1. Connect the IO-Link Master to the PC through **local wired Ethernet**.
2. Configure the PC/Master network so the correct **Master IP address is reachable on the local subnet**.
3. At the same time, keep the PC connected to a working **Internet connection, typically through Wi-Fi**.
4. On the **initial ICEops startup**, an IODD update prompt is displayed. With Internet access available, choose **Update/Yes** so ICEops can synchronize the latest available IODD data.
5. After the initial synchronization, you do **not** need to press the IODD Update button on every normal startup.
6. When a **new IO-Link device is added later**, press the **IODD Update** button to explicitly refresh the IODD catalog before commissioning or production use.
7. Confirm device identification, IODD availability, and process-data mapping before continuing with a newly added device.

> **INITIAL STARTUP:** ICEops asks whether to update IODD data. Keep Internet access available and approve the update to synchronize the latest IODD catalog.
>
> **NEW DEVICE:** If you add a new IO-Link device after the initial setup, press **IODD Update** to refresh the catalog, then confirm Device Identification and Mapping before use.
>
> **필수:** Master는 로컬 유선 Ethernet에서 올바른 Master IP로 연결하고, PC는 동시에 Wi-Fi 등으로 정상적인 인터넷 연결을 유지하십시오. **ICEops 최초 실행 시 IODD 업데이트 여부를 묻는 팝업이 표시됩니다. 인터넷이 연결된 상태에서 Update/Yes를 선택하여 최신 IODD 데이터를 동기화하십시오.** 초기 동기화 이후에는 정상 실행 때마다 IODD Update 버튼을 누를 필요가 없습니다. 단, 기존 환경에 **신규 IO-Link Device를 추가한 경우에는 IODD Update 버튼을 눌러 최신 IODD Catalog를 갱신한 뒤** Device Identification/Mapping을 확인하고 사용하십시오.

Recommended topology:

```text
Local Ethernet
PC ───────────── IO-Link Master
     Master IP / Local subnet

Wi-Fi / Internet
PC ───────────── Internet
     Initial IODD synchronization

Initial startup
ICEops ───────── IODD update prompt
                 Update/Yes → synchronize catalog

New device added later
ICEops ───────── IODD Update button
                 Explicit catalog refresh
```

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
- **네트워크/IODD 필수 안내:** Master는 로컬 유선 Ethernet에서 올바른 Master IP로 연결하고, PC는 Wi-Fi 등으로 인터넷 연결을 유지하십시오. **ICEops 최초 실행 시 IODD 업데이트 여부를 묻는 팝업이 표시되며, 인터넷이 연결되어 있다면 Update/Yes를 선택하여 최신 IODD 데이터를 동기화하십시오.** 초기 동기화 후에는 정상 실행 때마다 IODD Update 버튼을 누를 필요가 없습니다. 단, 기존 환경에 **신규 IO-Link Device를 추가한 경우에는 IODD Update 버튼을 눌러 Catalog를 갱신한 뒤** Device Identification과 Mapping을 확인하고 사용하십시오.

## English

This is the official download and automatic update repository for ICEops.

- Download the latest installer from **Releases**.
- Use only installers published in this repository.
- Automatic updates verify the installer with SHA-256 before installation.
- This repository contains deployment files only. Source code is not distributed here.
- A Windows 11 64-bit system with 32 GB RAM, NVMe SSD, 1 GbE wired networking, and ASUS NUC 15 Pro-class hardware or better is recommended.
- When running local Expert 14B AI on the same PC, an NVIDIA RTX-class GPU is recommended for practical response speed.
- **Network/IODD requirement:** Connect the Master over local wired Ethernet using the correct Master IP and keep Internet access available through Wi-Fi or another Internet connection. **On the initial ICEops startup, an IODD update prompt is displayed; with Internet access available, select Update/Yes to synchronize the latest IODD data.** After the initial synchronization, manual IODD Update is not required on every normal startup. If a **new IO-Link device is added later**, press **IODD Update** to explicitly refresh the catalog, then confirm device identification and mapping before use.

## Deutsch

Dieses Repository ist das offizielle Download- und automatische Update-Repository für ICEops.

- Laden Sie das neueste Installationsprogramm unter **Releases** herunter.
- Verwenden Sie ausschließlich Installationsprogramme, die in diesem Repository veröffentlicht wurden.
- Automatische Updates überprüfen das Installationsprogramm vor der Installation mit SHA-256.
- Dieses Repository enthält ausschließlich Bereitstellungsdateien. Der Quellcode wird hier nicht veröffentlicht.
- Empfohlen werden Windows 11 64-Bit, 32 GB RAM, eine NVMe-SSD, kabelgebundenes 1-GbE-Netzwerk und Hardware der Klasse ASUS NUC 15 Pro oder besser.
- Für den lokalen Expert-14B-KI-Betrieb auf demselben PC wird für praxisgerechte Antwortzeiten eine NVIDIA-RTX-GPU empfohlen.
- **Netzwerk-/IODD-Hinweis:** Verbinden Sie den Master über lokales kabelgebundenes Ethernet mit der korrekten Master-IP und halten Sie gleichzeitig eine Internetverbindung über WLAN oder eine andere Internetverbindung aufrecht. **Beim ersten Start von ICEops wird ein Dialog zur IODD-Aktualisierung angezeigt. Wenn Internetzugang verfügbar ist, wählen Sie Update/Ja, um die neuesten IODD-Daten zu synchronisieren.** Nach der ersten Synchronisierung ist ein manueller IODD Update nicht bei jedem normalen Start erforderlich. Wenn später ein **neues IO-Link-Gerät hinzugefügt** wird, drücken Sie **IODD Update**, um den Katalog gezielt zu aktualisieren, und prüfen Sie anschließend Geräteidentifikation und Mapping.

## 日本語

このリポジトリは、ICEops の公式インストーラーおよび自動アップデート配布用リポジトリです。

- 最新のインストーラーは **Releases** からダウンロードしてください。
- このリポジトリで公開された公式インストーラーのみを使用してください。
- 自動アップデートでは、インストール前に SHA-256 による整合性確認を行います。
- このリポジトリには配布ファイルのみが含まれ、ソースコードは公開されません。
- Windows 11 64-bit、32 GB RAM、NVMe SSD、1 GbE 有線ネットワーク、および ASUS NUC 15 Pro クラス以上のシステムを推奨します。
- 同一PCでローカル Expert 14B AI を使用する場合は、実用的な応答速度のため NVIDIA RTX クラスの GPU を推奨します。
- **ネットワーク/IODD 必須事項:** Master は正しい Master IP を設定したローカル有線 Ethernet で接続し、PC は Wi-Fi などでインターネット接続を維持してください。**ICEops の初回起動時には IODD 更新確認のポップアップが表示されます。インターネット接続がある状態で Update/Yes を選択し、最新の IODD データを同期してください。** 初回同期後は通常起動のたびに IODD Update を実行する必要はありません。後から **新しい IO-Link Device を追加した場合**は、**IODD Update** ボタンを押して Catalog を明示的に更新し、Device Identification と Mapping を確認してから使用してください。

## 中文

本仓库是 ICEops 官方安装程序及自动更新发布仓库。

- 请从 **Releases** 下载最新安装程序。
- 请仅使用本仓库发布的官方安装程序。
- 自动更新会在安装前通过 SHA-256 验证文件完整性。
- 本仓库仅包含发布文件，不提供源代码。
- 推荐使用 Windows 11 64 位、32 GB RAM、NVMe SSD、1 GbE 有线网络以及 ASUS NUC 15 Pro 级别或更高配置的系统。
- 如果在同一台电脑上运行本地 Expert 14B AI，为获得实用的响应速度，建议使用 NVIDIA RTX 级 GPU。
- **网络/IODD 必要说明：** 使用正确的 Master IP 通过本地有线 Ethernet 连接 Master，同时通过 Wi-Fi 或其他方式保持互联网连接。**ICEops 首次启动时会显示是否更新 IODD 的提示窗口；在互联网连接可用时请选择 Update/Yes，以同步最新 IODD 数据。** 完成首次同步后，无需每次正常启动都手动执行 IODD Update。如果之后**新增 IO-Link Device**，请按 **IODD Update** 按钮显式刷新 Catalog，并在使用前确认 Device Identification 和 Mapping。

## Español

Este es el repositorio oficial de descarga y actualización automática de ICEops.

- Descargue el instalador más reciente desde **Releases**.
- Utilice únicamente los instaladores publicados en este repositorio.
- Las actualizaciones automáticas verifican el instalador mediante SHA-256 antes de la instalación.
- Este repositorio contiene únicamente archivos de distribución. El código fuente no se publica aquí.
- Se recomienda Windows 11 de 64 bits, 32 GB de RAM, SSD NVMe, red Ethernet cableada de 1 GbE y hardware de clase ASUS NUC 15 Pro o superior.
- Para ejecutar AI Expert 14B localmente en el mismo PC, se recomienda una GPU NVIDIA de clase RTX para obtener tiempos de respuesta prácticos.
- **Requisito de red/IODD:** Conecte el Master por Ethernet cableado local usando la IP correcta del Master y mantenga acceso a Internet mediante Wi-Fi u otra conexión. **En el primer inicio de ICEops se muestra un aviso para actualizar los datos IODD; con acceso a Internet disponible, seleccione Update/Yes para sincronizar los datos IODD más recientes.** Después de la sincronización inicial, no es necesario ejecutar manualmente IODD Update en cada inicio normal. Si posteriormente se añade un **nuevo dispositivo IO-Link**, pulse **IODD Update** para actualizar explícitamente el catálogo y confirme la identificación y el mapping antes de usarlo.

## Repository contents

- Release installers
- SHA-256 checksum files
- `update.json` update metadata

ICEops source code, signing keys, license tools, and private build assets are not stored here.
