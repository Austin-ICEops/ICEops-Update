# ICEops Update Repository

> Official ICEops installer, release package, and automatic update repository.

## 🚨 REQUIRED BEFORE FIRST CONNECTION — Enable Modbus TCP and Update IODD

**Complete this sequence before the first ICEops Master connection. Also repeat the IODD Update step whenever the connected IO-Link device lineup changes.**

1. Connect the PC to the IO-Link Master network.
2. Keep the PC connected to the Internet as well, typically through Wi-Fi, so IODD synchronization can complete.
3. Start **ICEops** and enter the correct **Master IP address** in the target/IP field.
4. **Do not connect ICEops to the Master yet.**
5. Click the **globe icon in the upper-left corner**. ICEops opens the **Master Web interface** using the entered Master IP even while ICEops is disconnected.
6. In Master Web, open **Config → Modbus TCP**.
7. At the bottom of the page, select/enable **Modbus Enable**.
8. Click **Save** and confirm that the setting has been applied.
9. Return to ICEops while it is still disconnected from the Master.
10. With the IO-Link devices physically connected to the Master, click the **IODD Update** button in ICEops.
11. **Wait until the IODD update has completed successfully. Do not connect to the Master while the IODD update is still running.**
12. After the IODD update is complete, connect ICEops to the Master normally.
13. Confirm Device Identification, IODD availability, and process-data mapping before commissioning or production use.

> **IMPORTANT:** The required first-start order is **Master Web → Modbus Enable → Save → IODD Update → wait for completion → Connect**.
>
> You can also open a normal web browser and enter the **Master IP address directly** to access the same Master Web interface.
>
> After initial setup, the **globe icon** remains available at any time to reopen Master Web and review or change the Master's internal settings, whether ICEops is currently connected or not, as long as a reachable Master IP is entered.
>
> **가장 먼저 해야 할 설정:** PC를 IO-Link Master 네트워크에 연결하고 인터넷도 사용 가능한 상태로 유지한 뒤 **ICEops를 실행하고 Master IP를 먼저 입력**하십시오. 이 단계에서는 **ICEops를 Master에 Connect하지 마십시오.** 왼쪽 상단의 **지구 모양 아이콘**으로 Master Web에 접속하여 **Config → Modbus TCP → Modbus Enable → Save**를 완료합니다. 그 다음 ICEops로 돌아와 **연결된 IO-Link Device가 장착된 상태에서 IODD Update 버튼을 누르고 업데이트가 완전히 완료될 때까지 기다린 후에 Master에 Connect**하십시오.
>
> 즉, 초기 연결 순서는 **Modbus Web Enable → Save → IODD Update → 완료 확인 → Connect**입니다. 신규 IO-Link Device를 추가하거나 연결 구성이 변경된 경우에도 Connect 전에 IODD Update를 다시 실행하고 완료를 확인하는 것을 권장합니다.
>
> 일반 웹 브라우저 주소창에 **Master IP를 직접 입력**해도 동일한 Master Web에 접속할 수 있습니다. 초기 설정 이후에도 ICEops의 지구 모양 아이콘은 연결 여부와 관계없이, 유효한 Master IP가 입력되어 있고 네트워크에서 접근 가능하면 언제든지 Master 내부 설정 확인/변경에 사용할 수 있습니다.
>
> **最優先の初期設定:** PC を IO-Link Master ネットワークへ接続し、インターネット接続も利用可能な状態にしてください。ICEops を起動して Master IP を入力しますが、**まだ Master には Connect しないでください。** 左上の地球アイコンから Master Web を開き、**Config → Modbus TCP → Modbus Enable → Save** を完了します。その後 ICEops に戻り、接続されている IO-Link Device が装着された状態で **IODD Update** を実行し、更新が正常に完了したことを確認してから Master に Connect してください。
>
> 初回接続の順序は **Modbus Web Enable → Save → IODD Update → 完了確認 → Connect** です。新しい IO-Link Device を追加した場合やデバイス構成を変更した場合も、Connect 前に IODD Update を再実行してください。

## ⚠️ REQUIRED: Master Network & IODD Initialization

**Use the local network for the Master and keep Internet access available for IODD synchronization.**

1. Connect the IO-Link Master to the PC through **local wired Ethernet**.
2. Configure the PC/Master network so the correct **Master IP address is reachable on the local subnet**.
3. At the same time, keep the PC connected to a working **Internet connection, typically through Wi-Fi**.
4. Before the first Master connection, complete **Modbus Enable** in Master Web as described above.
5. Before pressing **Connect**, click **IODD Update** in ICEops with the intended IO-Link devices connected to the Master.
6. Wait until the IODD synchronization reports completion/success.
7. Only after the update has completed, connect ICEops to the Master and confirm Device Identification, IODD availability, and process-data mapping.
8. If the device lineup is unchanged and the IODD catalog is already synchronized, a manual update is not required on every normal reconnect.
9. Whenever a **new IO-Link device is added or the connected device lineup changes**, run **IODD Update before connecting/commissioning that configuration**.

> **INITIAL STARTUP:** Keep Internet access available and complete IODD Update before the first Master connection. If the startup update prompt appears, approve it and allow synchronization to finish before connecting.
>
> **NEW OR CHANGED DEVICE CONFIGURATION:** Run **IODD Update** with the devices connected, wait for completion, then connect/commission and verify Device Identification and Mapping.
>
> **필수:** Master는 로컬 유선 Ethernet에서 올바른 Master IP로 연결하고, PC는 동시에 Wi-Fi 등으로 정상적인 인터넷 연결을 유지하십시오. **최초 Master 연결 전에는 Master Web에서 Modbus Enable을 먼저 완료하고, ICEops에서 연결된 Device 기준으로 IODD Update 버튼을 눌러 업데이트가 완료된 것을 확인한 뒤 Connect하십시오.** 초기 동기화 후 동일한 Device 구성으로 정상 재접속할 때마다 수동 업데이트할 필요는 없습니다. 다만 **신규 IO-Link Device가 추가되거나 Device 구성이 변경되면 Connect/Commissioning 전에 IODD Update를 다시 실행하고 완료를 확인**하십시오.

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

        └─ Return to ICEops
           Connected IO-Link devices installed
           IODD Update → WAIT UNTIL COMPLETE
                         │
                         └─ Connect ICEops to Master

Required order
Modbus Web Enable → Save → IODD Update → Complete → Connect

Alternative initial access
Browser → Master IP → Master Web

Local Ethernet
PC ───────────── IO-Link Master
     Master IP / Local subnet

Wi-Fi / Internet
PC ───────────── Internet
     IODD synchronization
     Software / patch update check

Device lineup changed
ICEops ───────── IODD Update button
                 Wait for completion
                 Then Connect / Commission

Any time after Master IP is entered
Globe icon ───── Master Web
                 Available even while ICEops is disconnected
                 Review/change Master internal settings

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
| Display | 1920×1080 minimum, 2560×1440,1600 recommended |
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
- **최초 연결 필수 순서:** ICEops를 실행하고 Master IP를 입력한 뒤 **아직 Master에 Connect하지 않은 상태에서** 왼쪽 상단 지구 모양 아이콘으로 Master Web에 접속합니다. **Config → Modbus TCP → Modbus Enable → Save**를 완료한 다음 ICEops로 돌아와, **연결된 IO-Link Device 기준으로 IODD Update 버튼을 누르고 업데이트가 완전히 완료된 것을 확인한 뒤 Connect**하십시오. 순서는 **Modbus Web Enable → Save → IODD Update → 완료 확인 → Connect**입니다.
- **네트워크/IODD 필수 안내:** Master는 로컬 유선 Ethernet에서 올바른 Master IP로 연결하고, PC는 Wi-Fi 등으로 인터넷 연결을 유지하십시오. 초기 IODD 동기화가 완료되고 Device 구성이 바뀌지 않았다면 정상 재접속 때마다 수동 IODD Update를 실행할 필요는 없습니다. 단, **신규 IO-Link Device 추가 또는 Device 구성 변경 시에는 Connect/Commissioning 전에 IODD Update를 다시 실행하고 완료를 확인한 뒤** Device Identification과 Mapping을 확인하십시오.
- **소프트웨어/패치 자동 업데이트:** PC가 인터넷에 연결되어 있으면 ICEops가 새로운 소프트웨어 버전 또는 패치 유무를 확인합니다. **업데이트가 있으면 업데이트할지 묻는 팝업이 표시되며, Update/Yes를 선택하면 다운로드, SHA-256 검증 및 업데이트가 자동으로 진행됩니다.**

## English

This is the official download and automatic update repository for ICEops.

- Download the latest installer from **Releases**.
- Use only installers published in this repository.
- Automatic updates verify the installer with SHA-256 before installation.
- This repository contains deployment files only. Source code is not distributed here.
- A Windows 11 64-bit system with 32 GB RAM, NVMe SSD, 1 GbE wired networking, and ASUS NUC 15 Pro-class hardware or better is recommended.
- When running local Expert 14B AI on the same PC, an NVIDIA RTX-class GPU is recommended for practical response speed.
- **Required first-connection sequence:** Start ICEops, enter the Master IP, and **do not connect yet**. Open Master Web from the upper-left globe icon and complete **Config → Modbus TCP → Modbus Enable → Save**. Return to ICEops, click **IODD Update** with the intended IO-Link devices connected, **wait until the update has completed successfully**, and only then connect to the Master. Required order: **Modbus Web Enable → Save → IODD Update → Complete → Connect**.
- **Network/IODD requirement:** Connect the Master over local wired Ethernet using the correct Master IP and keep Internet access available through Wi-Fi or another Internet connection. A manual IODD update is not required on every normal reconnect once the catalog is synchronized and the device lineup is unchanged. If a **new IO-Link device is added or the device lineup changes**, run **IODD Update before Connect/Commissioning**, wait for completion, then confirm device identification and mapping.
- **Automatic software/patch updates:** When the PC has Internet access, ICEops checks for newer software versions and patches. **If an update is available, ICEops displays a confirmation popup. Select Update/Yes and ICEops automatically downloads, verifies with SHA-256, and applies the update.**

## Deutsch

Dieses Repository ist das offizielle Download- und automatische Update-Repository für ICEops.

- Laden Sie das neueste Installationsprogramm unter **Releases** herunter.
- Verwenden Sie ausschließlich Installationsprogramme, die in diesem Repository veröffentlicht wurden.
- Automatische Updates überprüfen das Installationsprogramm vor der Installation mit SHA-256.
- Dieses Repository enthält ausschließlich Bereitstellungsdateien. Der Quellcode wird hier nicht veröffentlicht.
- Empfohlen werden Windows 11 64-Bit, 32 GB RAM, eine NVMe-SSD, kabelgebundenes 1-GbE-Netzwerk und Hardware der Klasse ASUS NUC 15 Pro oder besser.
- Für den lokalen Expert-14B-KI-Betrieb auf demselben PC wird für praxisgerechte Antwortzeiten eine NVIDIA-RTX-GPU empfohlen.
- **Erforderliche Reihenfolge vor der ersten Verbindung:** Starten Sie ICEops, geben Sie die Master-IP ein und **verbinden Sie ICEops noch nicht mit dem Master**. Öffnen Sie über das Globus-Symbol Master Web und führen Sie **Config → Modbus TCP → Modbus Enable → Save** aus. Kehren Sie zu ICEops zurück, führen Sie mit den angeschlossenen IO-Link-Geräten **IODD Update** aus, warten Sie bis die Aktualisierung vollständig abgeschlossen ist und stellen Sie erst danach die Verbindung zum Master her. Reihenfolge: **Modbus Web Enable → Save → IODD Update → Abschluss → Connect**.
- **Netzwerk-/IODD-Hinweis:** Verbinden Sie den Master über lokales kabelgebundenes Ethernet mit der korrekten Master-IP und halten Sie gleichzeitig eine Internetverbindung über WLAN oder eine andere Internetverbindung aufrecht. Wenn der IODD-Katalog synchronisiert ist und die Gerätekonfiguration unverändert bleibt, ist nicht bei jeder normalen Wiederverbindung ein manuelles Update erforderlich. Wenn ein **neues IO-Link-Gerät hinzugefügt oder die Gerätekonfiguration geändert** wird, führen Sie **IODD Update vor Connect/Inbetriebnahme** aus, warten Sie auf den Abschluss und prüfen Sie anschließend Geräteidentifikation und Mapping.
- **Automatische Software-/Patch-Updates:** Bei bestehender Internetverbindung prüft ICEops auf neue Softwareversionen und Patches. **Wenn ein Update verfügbar ist, wird ein Bestätigungsdialog angezeigt. Nach Auswahl von Update/Ja lädt ICEops das Update automatisch herunter, prüft es mit SHA-256 und installiert es.**

## 日本語

このリポジトリは、ICEops の公式インストーラーおよび自動アップデート配布用リポジトリです。

- 最新のインストーラーは **Releases** からダウンロードしてください。
- このリポジトリで公開された公式インストーラーのみを使用してください。
- 自動アップデートでは、インストール前に SHA-256 による整合性確認を行います。
- このリポジトリには配布ファイルのみが含まれ、ソースコードは公開されません。
- Windows 11 64-bit、32 GB RAM、NVMe SSD、1 GbE 有線ネットワーク、および ASUS NUC 15 Pro クラス以上のシステムを推奨します。
- 同一PCでローカル Expert 14B AI を使用する場合は、実用的な応答速度のため NVIDIA RTX クラスの GPU を推奨します。
- **初回接続の必須手順:** ICEops を起動して Master IP を入力し、**まだ Master には Connect しないでください。** 左上の地球アイコンから Master Web を開き、**Config → Modbus TCP → Modbus Enable → Save** を完了します。その後 ICEops に戻り、接続されている IO-Link Device に対して **IODD Update** を実行し、**更新が正常に完了したことを確認してから** Master に Connect してください。順序は **Modbus Web Enable → Save → IODD Update → 完了確認 → Connect** です。
- **ネットワーク/IODD 必須事項:** Master は正しい Master IP を設定したローカル有線 Ethernet で接続し、PC は Wi-Fi などでインターネット接続を維持してください。IODD Catalog が同期済みで Device 構成が変わっていない通常の再接続では、毎回 IODD Update を行う必要はありません。**新しい IO-Link Device の追加または Device 構成の変更時**は、Connect/Commissioning 前に **IODD Update** を実行し、完了後に Device Identification と Mapping を確認してください。
- **ソフトウェア/パッチ自動更新:** PC がインターネットに接続されている場合、ICEops は新しいソフトウェアバージョンまたはパッチを確認します。**更新がある場合は確認ポップアップが表示され、Update/Yes を選択すると自動的にダウンロード、SHA-256 検証、更新が実行されます。**

## 中文

本仓库是 ICEops 官方安装程序及自动更新发布仓库。

- 请从 **Releases** 下载最新安装程序。
- 请仅使用本仓库发布的官方安装程序。
- 自动更新会在安装前通过 SHA-256 验证文件完整性。
- 本仓库仅包含发布文件，不提供源代码。
- 推荐使用 Windows 11 64 位、32 GB RAM、NVMe SSD、1 GbE 有线网络以及 ASUS NUC 15 Pro 级别或更高配置的系统。
- 如果在同一台电脑上运行本地 Expert 14B AI，为获得实用的响应速度，建议使用 NVIDIA RTX 级 GPU。
- **首次连接前的必需顺序：** 启动 ICEops 并输入 Master IP，**此时不要连接 Master**。通过左上角的地球图标打开 Master Web，完成 **Config → Modbus TCP → Modbus Enable → Save**。返回 ICEops，在目标 IO-Link Device 已连接的状态下执行 **IODD Update**，**等待更新成功完成后**再连接 Master。顺序为 **Modbus Web Enable → Save → IODD Update → 完成确认 → Connect**。
- **网络/IODD 必要说明：** 使用正确的 Master IP 通过本地有线 Ethernet 连接 Master，同时通过 Wi-Fi 或其他方式保持互联网连接。IODD Catalog 已同步且 Device 配置未变化时，正常重新连接无需每次手动更新。如果**新增 IO-Link Device 或 Device 配置发生变化**，请在 Connect/Commissioning 前执行 **IODD Update**，等待完成后再确认 Device Identification 和 Mapping。
- **软件/补丁自动更新：** PC 连接互联网后，ICEops 会检查新的软件版本或补丁。**如果有可用更新，会显示确认弹窗；选择 Update/Yes 后，ICEops 会自动下载、执行 SHA-256 校验并完成更新。**

## Español

Este es el repositorio oficial de descarga y actualización automática de ICEops.

- Descargue el instalador más reciente desde **Releases**.
- Utilice únicamente los instaladores publicados en este repositorio.
- Las actualizaciones automáticas verifican el instalador mediante SHA-256 antes de la instalación.
- Este repositorio contiene únicamente archivos de distribución. El código fuente no se publica aquí.
- Se recomienda Windows 11 de 64 bits, 32 GB de RAM, SSD NVMe, red Ethernet cableada de 1 GbE y hardware de clase ASUS NUC 15 Pro o superior.
- Para ejecutar AI Expert 14B localmente en el mismo PC, se recomienda una GPU NVIDIA de clase RTX para obtener tiempos de respuesta prácticos.
- **Secuencia obligatoria antes de la primera conexión:** Inicie ICEops, introduzca la IP del Master y **no conecte todavía**. Abra Master Web mediante el icono de globo y complete **Config → Modbus TCP → Modbus Enable → Save**. Vuelva a ICEops, ejecute **IODD Update** con los dispositivos IO-Link previstos conectados, **espere hasta que la actualización termine correctamente** y solo entonces conecte al Master. Orden: **Modbus Web Enable → Save → IODD Update → Completado → Connect**.
- **Requisito de red/IODD:** Conecte el Master por Ethernet cableado local usando la IP correcta del Master y mantenga acceso a Internet mediante Wi-Fi u otra conexión. Si el catálogo IODD ya está sincronizado y la configuración de dispositivos no ha cambiado, no es necesario ejecutar una actualización manual en cada reconexión normal. Si se **añade un nuevo dispositivo IO-Link o cambia la configuración de dispositivos**, ejecute **IODD Update antes de Connect/Commissioning**, espere a que termine y confirme la identificación y el mapping antes del uso.
- **Actualizaciones automáticas de software/parches:** Cuando el PC dispone de acceso a Internet, ICEops busca nuevas versiones de software y parches. **Si hay una actualización disponible, aparece un cuadro de confirmación. Al seleccionar Update/Yes, ICEops descarga, verifica mediante SHA-256 y aplica la actualización automáticamente.**

## Repository contents

- Release installers
- SHA-256 checksum files
- `update.json` update metadata

ICEops source code, signing keys, license tools, and private build assets are not stored here.