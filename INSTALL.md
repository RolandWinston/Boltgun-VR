# 安装与启动

准备 Steam 版《Warhammer 40,000: Boltgun》、Windows x64、Python 3.10 或更新版本。打开 Steam，连接头显，启动 SteamVR，并将 SteamVR 设为当前 OpenXR 运行环境。

从 [praydog 的 UEVR nightly 发布页](https://github.com/praydog/UEVR-nightly/releases/tag/nightly-01143-4ee5c6b6162dee2291fc75f9dfc57667f6d45a2d) 下载并解压 nightly 01143。运行一次 UEVR，选择 OpenXR，然后关闭注入器。

从本项目发布页下载 Boltgun-VR-v23.0.0.zip，解压到自己的文件夹。打开该文件夹的终端，先检查文件：

```powershell
python launch.py --check
```

找到游戏目录内的 Boltgun/Binaries/Win64/Boltgun-Win64-Shipping.exe，以及 UEVR 文件夹内的 UEVRInjector.exe。将下面两处路径换成自己的实际位置，然后执行：

```powershell
python launch.py --game "D:\SteamLibrary\steamapps\common\Boltgun\Boltgun\Binaries\Win64\Boltgun-Win64-Shipping.exe" --uevr "D:\UEVR-nightly-01143\UEVRInjector.exe"
```

游戏启动后自动请求 UEVR 注入。保持终端打开，在游戏中选择继续或开始新游戏。退出游戏后，终端会显示配置恢复完成。游戏进度按原版规则保存。

可以将填好路径的命令保存为自己的启动脚本。运行前关闭已有的 Boltgun 和 UEVR 注入器。

## 备份与恢复

每次启动使用独立会话。旧 VR 配置临时保存在原目录旁的 Boltgun-Win64-Shipping.backup-* 文件夹。退出时自动还原。

会话记录位于 %LOCALAPPDATA%/BoltgunVR/sessions。每个会话保存 transaction.json、原 Input.ini 和本轮 VR 配置。运行文件存放在本机。

如果终端或电脑在游戏运行期间意外关闭：先退出 Boltgun 和 UEVR；按照 transaction.json 中的 profile 与 backup 路径，将当前会话配置移到备份位置，再将 backup 文件夹改回原 profile 名称；将 Input.ini.before 复制回 transaction.json 中的 input 路径。input_existed 为 false 时，移走本轮创建的 Input.ini。

## English setup

Install your own Steam copy of Boltgun, Python 3.10+ and the official UEVR nightly 01143. Connect the headset, start SteamVR and select SteamVR as the active OpenXR runtime. Select OpenXR in the UEVR frontend, then close it.

Extract the release ZIP, run `python launch.py --check`, then run the launch command above with your actual game and injector paths. Keep the terminal open until the game exits. Your original VR profile and Input.ini are restored after the session; game saves remain under the game's normal control.

The launcher checks the exact game and UEVR build before installing the session. Compatibility details and recovery boundaries are in [release notes](RELEASE-NOTES.md).
