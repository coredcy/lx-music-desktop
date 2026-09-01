# LX Music Desktop：自定义音源配置 Fork

这是 [LX Music Desktop](https://github.com/lyswhut/lx-music-desktop) 的个人 Fork，用于保留可复用的自定义音源配置，并提供打包后应用的导入说明。

原项目的完整功能介绍、构建说明、常见问题与发布版本，请参阅上游仓库的 [README](https://github.com/lyswhut/lx-music-desktop#readme)。

## 此 Fork 的改动

- 新增 [`custom-sources/user_api.json`](./custom-sources/user_api.json)：当前保留的 11 个 LX Music 自定义源配置。
- 新增 [`custom-sources/README.md`](./custom-sources/README.md)：说明如何将该配置用于打包后的安装版或便携版应用。

除上述自定义音源配置与文档外，当前没有修改上游应用的功能逻辑。

## 使用自定义源

请按 [`custom-sources/README.md`](./custom-sources/README.md) 的步骤操作。简要流程是：

1. 首次启动打包后的应用一次后完全退出。
2. 备份目标数据目录中的 `LxDatas/user_api.json`。
3. 用本仓库的 [`custom-sources/user_api.json`](./custom-sources/user_api.json) 覆盖该文件。
4. 重新启动应用，并在“设置 → 自定义源管理”确认源列表。

该操作会替换目标应用原有的全部自定义源，不会与已有配置合并。

## 说明

- 自定义源均为第三方脚本；它们的可用性可能随平台、歌曲、音质或服务端状态变化。
- 仅导入你信任的源，并在更新配置前备份自己的 `user_api.json`。
- 本 Fork 继续遵循上游项目的 [Apache-2.0 License](./LICENSE)。

## 上游与同步

- 上游仓库：[lyswhut/lx-music-desktop](https://github.com/lyswhut/lx-music-desktop)
- 本 Fork 的目的仅是维护自定义源配置；需要上游功能、发行版或问题支持时，请优先查阅上游仓库。
