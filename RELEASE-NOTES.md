# v23.0.0 配套说明

## 版本与范围

此版本以本机 v23-rc1 的 release-candidate-02 为基础。2026-10-27 用户完成头显测试，反馈「都测试了，目前没什么太大问题」，并明确要求发布到 GitHub。本版公开编号为 v23.0.0。

模型、四个运行插件和生产逻辑保持已测版本。分发调整包含相对运行依赖路径、便携启动器和安装说明。测试用的自动全武器脚本移到 extras，普通启动使用玩家自己的库存与存档。extras 仅供开发测试；自动授予武器会改变库存，不要复制到普通 profile。

公开启动器完成现有配置、首次安装、安装中断恢复、进程时间标识与包完整性检查。本机最终头显验收使用原有本机入口；公开便携入口尚未在第二台电脑做完整头显验收。

## 检查结果

八把基础武器完成原生射击检查，31 颗生成弹丸逐颗核对枪口位置和方向。三种手雷完成原生投掷检查。爆燃机枪和重力枪分别通过原生敌人命中与击杀检查；四段射击的八张左右眼提交图像完成检查。重力枪主束起点最大采样偏差为 0.084 厘米。热熔枪保留原有正常行为。

追踪丢失和恢复、暂停与返回、正常退出与配置恢复完成回归。最新用户会话正常退出，原有配置、输入和存档恢复校验通过。

用户验收代表该用户设备上的实际反馈，不代表固定帧率保证。早期代理环境测得约每秒 29.57 至 32.29 次引擎更新；该指标不是头显显示帧率。性能随显卡、分辨率和串流设置变化。

基础游戏的八把枪是本轮测试范围。Multi-Melta 和 Missile Launcher 保留模型，DLC 战斗未独立验收。其他头显与控制器映射未单独认证。

## 兼容性

Windows x64，游戏 UE4.27，UEVR nightly 01143，OpenXR。测试环境为 Quest 3、ALVR 20.14.1 和 SteamVR。运行层修正作用于本次游戏进程，不修改系统 OpenXR 注册表。

启动器验证游戏与 UEVRBackend.dll 的精确指纹。其他游戏更新或 UEVR 版本应先完成兼容性测试。manifest.json 保存对应指纹。

## English scope

Accepted by the user after Quest 3 headset testing on 27 October 2026. The gameplay binaries and production logic match the accepted build. Packaging adds relative runtime paths and a portable launcher; the inventory-grant test fixture is kept outside normal startup.

The portable launcher passed isolated backup/restore and package checks. It has not received a full headset acceptance run on a second PC. No fixed display frame rate is promised. Eight base-game weapons were tested; DLC combat and other controllers remain unverified.
