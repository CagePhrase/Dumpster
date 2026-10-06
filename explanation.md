# Dumpster 支持情况

> Windows 10/11 + macOS，Linux 暂不支持

| 平台 | 状态 | 说明 |
| :--- | :---: | :--- |
| **Windows 10/11 x64** | ✅ 已构建 · 已实测 | MSI / NSIS 安装包 |
| **macOS** | ⚠️ 配置就绪 · 未测试 | 有已知缺陷，见下 |
| **Linux** | ❌ 暂不支持 | 透明窗口依赖桌面合成器 |

## 各平台说明

### Windows 10/11 x64

- 已完成构建，并在真机上实测通过
- 产物：`Dumpster_0.0.1_x64_en-US.msi`、`Dumpster_0.0.1_x64-setup.exe`
- **注意**：不要从 OneDrive 同步目录中运行 exe，会因访问被拒而启动失败

### macOS

- 配置已就绪：`macos-private-api` 特性 + `macOSPrivateApi: true`（透明窗口前提）
- 但**尚未构建、尚未测试**
- 已知缺陷：日志路径写死了 Windows 专有的 `LOCALAPPDATA` 环境变量，macOS 上会回退到当前工作目录（通常不可写），导致日志静默失效
- 现实约束：macOS 版必须在 Mac 上构建，Tauri 不支持从 Windows 交叉编译

### Linux

- 明确不支持
- 透明窗口依赖桌面合成器，未做验证
