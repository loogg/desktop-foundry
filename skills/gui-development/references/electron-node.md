# 示例：Electron + Node 业务服务

适用：Electron 的 Web Renderer 通过 preload/IPC 访问 Node 服务，设备通信、缓存、文件或持久化主要在 Node 层。与桌面共用约束一起使用。

## 技术栈与架构

技术栈示例：Electron + React + TypeScript，构建可使用 Vite/electron-vite 或 Forge Vite。UI 可组合 Tailwind、Radix、Zustand、TanStack 表格/虚拟列表、ECharts 等，按项目需要选择。

```text
共享 Renderer → AppTransport / typed API
                 ├─ preload / IPC ─┐
                 └─ WebSocket ─────┴→ Backend Service → Runtime / 数据 / 设备
```

## 实现参考

- 可由 Node 服务管理通信、缓存与持久化，通过 Snapshot/delta、事件或其他符合契约的方式同步到 UI；具体分层按功能和运行条件确定。
- 图示使用 preload/IPC 与 WebSocket 适配同一业务服务。传输方式可按调用与事件需要调整；浏览器审查进程也可实例化相同业务实现，明确与原生运行的能力及数据差异。
- 离线解析等前端功能可在 Renderer 实现；共用协议定义与必要的编解码能力，避免同一业务规则重复维护。

## 启动核对与审查

1. 从项目脚本确认原生入口、Renderer 入口、Bridge 服务和所需模拟器，核对服务就绪、数据目录和自动连接行为；仅启动 Vite 不代表后端就绪。
2. 用鼠标/键盘完成本次流程，核对反馈、事件及约定的权威数据源，输入或 pending 不冒充确认结果。通信改动通过真实 Bridge 或原生通道对照实际服务/模拟器请求与结果，模拟反馈单独记录；纯前端功能按真实输入与预期结果验证，Fixture 不代替被测按钮。
3. 在真实 Electron 检查受影响的 preload/IPC、窗口和系统能力，涉及原生访问时核对权限与参数校验。已有项目只有浏览器模拟适配时，可先用原生审查本次功能并说明真实 Bridge 差距。
4. 沿用项目的逻辑、通信集成与原生回归工具，按影响范围选择。涉及原生模块或打包路径时核对构建与资源；生成交付包遵循桌面版本与打包的触发条件。
