# ICEops Update Repository

> Official ICEops installer, release package, and automatic update repository.

## 🚨 FIRST STEP BEFORE CONNECTING ICEops — Enable Modbus TCP on the Master

**This is the highest-priority setup step. Complete it before the first ICEops Master connection.**

1. Connect the PC to the IO-Link Master network.
2. Start **ICEops** and enter the correct **Master IP address** in the target/IP field.
3. **You do not need to connect ICEops to the Master yet.**
4. Click the **globe icon in the upper-left corner**. ICEops opens the **Master Web interface** using the entered Master IP even while ICEops is disconnected.
5. Open **Config → Modbus TCP**.
6. At the bottom of the page, select/enable **Modbus Enable**.
7. Click **Save** and confirm that the setting has been applied.
8. Return to ICEops and connect to the Master normally.

> **IMPORTANT:** The first Modbus TCP setup must be completed **before the first ICEops Master connection**, but ICEops itself may already be running. Enter the Master IP first, then use the globe icon to open Master Web without connecting.
>
> You can also open a normal web browser and enter the **Master IP address directly** to access the same Master Web interface.
>
> After initial setup, the **globe icon** remains available at any time to reopen Master Web and review or change the Master's internal settings, whether ICEops is currently connected or not, as long as a reachable Master IP is entered.
>
> **가장 먼저 해야 할 설정:** PC를 IO-Link Master 네트워크에 연결한 뒤 **ICEops를 실행하고 Master IP를 먼저 입력**하십시오. 이 단계에서는 **ICEops를 Master에 Connect할 필요가 없습니다.** 왼쪽 상단의 **지구 모양 아이콘**을 누르면 입력된 Master IP를 사용하여 바로 **Master Web**에 접속할 수 있습니다. **Config → Modbus TCP → Modbus Enable → Save** 순서로 설정을 완료한 뒤 ICEops에서 Master에 정상 연결하십시오.
>
> 일반 웹 브라우저 주소창에 **Master IP를 직접 입력**해도 동일한 Master Web에 접속할 수 있습니다. 초기 설정 이후에도 ICEops의 지구 모양 아이콘은 연결 여부와 관계없이, 유효한 Master IP가 입력되어 있고 네트워크에서 접근 가능하면 언제든지 Master 내부 설정 확인/변경에 사용할 수 있습니다.
>
> **最優先の設定:** PC を IO-Link Master のネットワークへ接続し、**ICEops を起動して Master IP を先に入力**してください。この時点では **ICEops を Master に Connect する必要はありません。** 左上の**地球アイコン**をクリックすると、入力した Master IP を使用して **Master Web** を開くことができます。**Config → Modbus TCP → Modbus Enable → Save** の順に設定し、その後 ICEops から Master へ通常接続してください。
>
> Web ブラウザに **Master IP を直接入力**して同じ Master Web を開くこともできます。初期設定後も、到達可能な Master IP が入力されていれば、ICEops の接続状態に関係なく地球アイコンから Master Web を開き、内部設定を確認・変更できます。

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

## 🔄 Software & Patch Updates

ICEops also supports **automatic software and patch updates through the Internet**.

- Keep the PC connected to the Internet through Wi-Fi or another available Internet connection.
- When a **new ICEops software version or patch is available**, ICEops displays an **update confirmation popup**.
- Select **Update/Yes** to allow ICEops to automatically download, verify, and apply the available update.
- The update package is verified with **SHA-256** before installation.
- Manual reinstallation is normally not required for updates delivered through the ICEops update mechanism.

> **SOFTWARE UPDATE:** If Internet access is available and a newer ICEops version or patch is detected, ICEops asks whether you want to update. Approve the popup and the update proceeds automatically.
>
> **소프트웨어/패치 업데이트:** PC가 인터넷에 연결되어 있으면 ICEops가 최신 소프트웨어 버전 또는 패치를 확인합니다. **새 업데이트가 있으면 업데이트할지 묻는 팝업이 표시되며, Update/Yes를 선택하면 다운로드, SHA-256 검증 및 업데이트가 자동으로 진행됩니다.**

Recommended topology:

```text
Before first ICEops Master connection
PC ───────────── IO-Link Master
ICEops: Enter Master IP
        │
        └─ Globe icon → Master Web
                         Config → Modbus TCP
                         Modbus Enable → Save
        (ICEops connection is NOT required yet)

Alternative initial access
Browser → Master IP → Master Web

Local Ethernet
PC ───────────── IO-Link Master
     Master IP / Local subnet

Wi-Fi / Internet
PC ───────────── Internet
     IODD synchronization
     Software / patch update check

Initial ICEops startup
ICEops ───────── IODD update prompt
                 Update/Yes → synchronize catalog

Any time after Master IP is entered
Globe icon ───── Master Web
                 Available even while ICEops is disconnected
                 Review/change Master internal settings

New device added later
ICEops ───────── IODD Update button
                 Explicit catalog refresh

New ICEops version / patch available
ICEops ───────── Update confirmation popup
                 Update/Yes → automatic update
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
- **최초 Modbus TCP 설정:** ICEops를 실행하고 Master IP를 입력한 뒤, **아직 Master에 연결하지 않은 상태에서도 왼쪽 상단 지구 모양 아이콘으로 Master Web에 접속할 수 있습니다.** Master Web에서 **Config → Modbus TCP → Modbus Enable → Save**를 완료한 후 ICEops에서 Master에 연결하십시오. 일반 브라우저에서 Master IP를 직접 입력하는 방법도 사용할 수 있습니다.
- **네트워크/IODD 필수 안내:** Master는 로컬 유선 Ethernet에서 올바른 Master IP로 연결하고, PC는 Wi-Fi 등으로 인터넷 연결을 유지하십시오. **ICEops 최초 실행 시 IODD 업데이트 여부를 묻는 팝업이 표시되며, 인터넷이 연결되어 있다면 Update/Yes를 선택하여 최신 IODD 데이터를 동기화하십시오.** 초기 동기화 후에는 정상 실행 때마다 IODD Update 버튼을 누를 필요가 없습니다. 단, 기존 환경에 **신규 IO-Link Device를 추가한 경우에는 IODD Update 버튼을 눌러 Catalog를 갱신한 뒤** Device Identification과 Mapping을 확인하고 사용하십시오.
- **소프트웨어/패치 자동 업데이트:** PC가 인터넷에 연결되어 있으면 ICEops가 새로운 소프트웨어 버전 또는 패치 유무를 확인합니다. **업데이트가 있으면 업데이트할지 묻는 팝업이 표시되며, Update/Yes를 선택하면 다운로드, SHA-256 검증 및 업데이트가 자동으로 진행됩니다.**

## English

This is the official download and automatic update repository for ICEops.

- Download the latest installer from **Releases**.
- Use only installers published in this repository.
- Automatic updates verify the installer with SHA-256 before installation.
- This repository contains deployment files only. Source code is not distributed here.
- A Windows 11 64-bit system with 32 GB RAM, NVMe SSD, 1 GbE wired networking, and ASUS NUC 15 Pro-class hardware or better is recommended.
- When running local Expert 14B AI on the same PC, an NVIDIA RTX-class GPU is recommended for practical response speed.
- **Initial Modbus TCP setup:** Start ICEops and enter the Master IP. **You can open Master Web from the upper-left globe icon even before ICEops is connected to the Master.** In Master Web, complete **Config → Modbus TCP → Modbus Enable → Save**, then connect ICEops normally. Direct browser access to the Master IP is also supported.
- **Network/IODD requirement:** Connect the Master over local wired Ethernet using the correct Master IP and keep Internet access available through Wi-Fi or another Internet connection. **On the initial ICEops startup, an IODD update prompt is displayed; with Internet access available, select Update/Yes to synchronize the latest IODD data.** After the initial synchronization, manual IODD Update is not required on every normal startup. If a **new IO-Link device is added later**, press **IODD Update** to explicitly refresh the catalog, then confirm device identification and mapping before use.
- **Automatic software/patch updates:** When the PC has Internet access, ICEops checks for newer software versions and patches. **If an update is available, ICEops displays a confirmation popup. Select Update/Yes and ICEops automatically downloads, verifies with SHA-256, and applies the update.**

## Deutsch

Dieses Repository ist das offizielle Download- und automatische Update-Repository für ICEops.

- Laden Sie das neueste Installationsprogramm unter **Releases** herunter.
- Verwenden Sie ausschließlich Installationsprogramme, die in diesem Repository veröffentlicht wurden.
- Automatische Updates überprüfen das Installationsprogramm vor der Installation mit SHA-256.
- Dieses Repository enthält ausschließlich Bereitstellungsdateien. Der Quellcode wird hier nicht veröffentlicht.
- Empfohlen werden Windows 11 64-Bit, 32 GB RAM, eine NVMe-SSD, kabelgebundenes 1-GbE-Netzwerk und Hardware der Klasse ASUS NUC 15 Pro oder besser.
- Für den lokalen Expert-14B-KI-Betrieb auf demselben PC wird für praxisgerechte Antwortzeiten eine NVIDIA-RTX-GPU empfohlen.
- **Netzwerk-/IODD-Hinweis:** Verbinden Sie den Master über lokales kabelgebundenes Ethernet mit der korrekten Master-IP und halten Sie gleichzeitig eine Internetverbindung über WLAN oder eine andere Internetverbindung aufrecht. **Beim ersten Start von ICEops wird ein Dialog zur IODD-Aktualisierung angezeigt. Wenn Internetzugang verfügbar ist, wählen Sie Update/Ja, um die neuesten IODD-Daten zu synchronisieren.** Nach der ersten Synchronisierung ist ein manueller IODD Update nicht bei jedem normalen Start erforderlich. Wenn später ein **neues IO-Link-Gerät hinzugefügt** wird, drücken Sie **IODD Update**, um den Katalog gezielt zu aktualisieren, und prüfen Sie anschließend Geräteidentifikation und Mapping.
- **Automatische Software-/Patch-Updates:** Bei bestehender Internetverbindung prüft ICEops auf neue Softwareversionen und Patches. **Wenn ein Update verfügbar ist, wird ein Bestätigungsdialog angezeigt. Nach Auswahl von Update/Ja lädt ICEops das Update automatisch herunter, prüft es mit SHA-256 und installiert es.**

## 日本語

このリポジトリは、ICEops の公式インストーラーおよび自動アップデート配布用リポジトリです。

- 最新のインストーラーは **Releases** からダウンロードしてください。
- このリポジトリで公開された公式インストーラーのみを使用してください。
- 自動アップデートでは、インストール前に SHA-256 による整合性確認を行います。
- このリポジトリには配布ファイルのみが含まれ、ソースコードは公開されません。
- Windows 11 64-bit、32 GB RAM、NVMe SSD、1 GbE 有線ネットワーク、および ASUS NUC 15 Pro クラス以上のシステムを推奨します。
- 同一PCでローカル Expert 14B AI を使用する場合は、実用的な応答速度のため NVIDIA RTX クラスの GPU を推奨します。
- **初回 Modbus TCP 設定:** ICEops を起動して Master IP を入力すれば、**まだ Master に接続していない状態でも左上の地球アイコンから Master Web を開くことができます。** Master Web で **Config → Modbus TCP → Modbus Enable → Save** を完了してから ICEops で Master に接続してください。Web ブラウザから Master IP を直接開く方法も使用できます。
- **ネットワーク/IODD 必須事項:** Master は正しい Master IP を設定したローカル有線 Ethernet で接続し、PC は Wi-Fi などでインターネット接続を維持してください。**ICEops の初回起動時には IODD 更新確認のポップアップが表示されます。インターネット接続がある状態で Update/Yes を選択し、最新の IODD データを同期してください。** 初回同期後は通常起動のたびに IODD Update を実行する必要はありません。後から **新しい IO-Link Device を追加した場合**は、**IODD Update** ボタンを押して Catalog を明示的に更新し、Device Identification と Mapping を確認してから使用してください。
- **ソフトウェア/パッチ自動更新:** PC がインターネットに接続されている場合、ICEops は新しいソフトウェアバージョンまたはパッチを確認します。**更新がある場合は確認ポップアップが表示され、Update/Yes を選択すると自動的にダウンロード、SHA-256 検証、更新が実行されます。**

## 中文

本仓库是 ICEops 官方安装程序及自动更新发布仓库。

- 请从 **Releases** 下载最新安装程序。
- 请仅使用本仓库发布的官方安装程序。
- 自动更新会在安装前通过 SHA-256 验证文件完整性。
- 本仓库仅包含发布文件，不提供源代码。
- 推荐使用 Windows 11 64 位、32 GB RAM、NVMe SSD、1 GbE 有线网络以及 ASUS NUC 15 Pro 级别或更高配置的系统。
- 如果在同一台电脑上运行本地 Expert 14B AI，为获得实用的响应速度，建议使用 NVIDIA RTX 级 GPU。
- **网络/IODD 必要说明：** 使用正确的 Master IP 通过本地有线 Ethernet 连接 Master，同时通过 Wi-Fi 或其他方式保持互联网连接。**ICEops 首次启动时会显示是否更新 IODD 的提示窗口；在互联网连接可用时请选择 Update/Yes，以同步最新 IODD 数据。** 完成首次同步后，无需每次正常启动都手动执行 IODD Update。如果之后**新增 IO-Link Device**，请按 **IODD Update** 按钮显式刷新 Catalog，并在使用前确认 Device Identification 和 Mapping。
- **软件/补丁自动更新：** PC 连接互联网后，ICEops 会检查新的软件版本或补丁。**如果有可用更新，会显示确认弹窗；选择 Update/Yes 后，ICEops 会自动下载、执行 SHA-256 校验并完成更新。**

## Español

Este es el repositorio oficial de descarga y actualización automática de ICEops.

- Descargue el instalador más reciente desde **Releases**.
- Utilice únicamente los instaladores publicados en este repositorio.
- Las actualizaciones automáticas verifican el instalador mediante SHA-256 antes de la instalación.
- Este repositorio contiene únicamente archivos de distribución. El código fuente no se publica aquí.
- Se recomienda Windows 11 de 64 bits, 32 GB de RAM, SSD NVMe, red Ethernet cableada de 1 GbE y hardware de clase ASUS NUC 15 Pro o superior.
- Para ejecutar AI Expert 14B localmente en el mismo PC, se recomienda una GPU NVIDIA de clase RTX para obtener tiempos de respuesta prácticos.
- **Requisito de red/IODD:** Conecte el Master por Ethernet cableado local usando la IP correcta del Master y mantenga acceso a Internet mediante Wi-Fi u otra conexión. **En el primer inicio de ICEops se muestra un aviso para actualizar los datos IODD; con acceso a Internet disponible, seleccione Update/Yes para sincronizar los datos IODD más recientes.** Después de la sincronización inicial, no es necesario ejecutar manualmente IODD Update en cada inicio normal. Si posteriormente se añade un **nuevo dispositivo IO-Link**, pulse **IODD Update** para actualizar explícitamente el catálogo y confirme la identificación y el mapping antes de usarlo.
- **Actualizaciones automáticas de software/parches:** Cuando el PC dispone de acceso a Internet, ICEops busca nuevas versiones de software y parches. **Si hay una actualización disponible, aparece un cuadro de confirmación. Al seleccionar Update/Yes, ICEops descarga, verifica mediante SHA-256 y aplica la actualización automáticamente.**

## Repository contents

- Release installers
- SHA-256 checksum files
- `update.json` update metadata

ICEops source code, signing keys, license tools, and private build assets are not stored here.