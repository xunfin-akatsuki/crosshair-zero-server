# crosshair-zero-server

准星：零点（Crosshair Zero）Minecraft 服务器配置存档。

由群里的月琉璃从线上实例整理导出，导出时间：2026-11-09，最近同步：2026-11-11（1.2.7 更新后按哈希重新对比过模组与配置）。

## 包含什么

- `config/`：服务端模组与插件的配置（toml / json / yml / properties / snbt 等文本）
- `defaultconfigs/`：默认配置模板
- `plugins/`：插件配置（不含插件本体）
- 根目录：`server.properties`、`bukkit.yml`、`spigot.yml`、`commands.yml`、白名单/OP/封禁名单、`eula.txt`
- `mods/mods.csv`：模组清单（文件名、SHA-256、字节数）
- `mods/plugins.csv`：插件清单（文件名、SHA-256、字节数）

## 不包含什么

- 模组和插件的 jar 文件本身，只保留名字和哈希，方便核对版本
- 世界存档、日志、备份、崩溃报告
- 缓存、价格快照、模型动画等运行数据
- 任何密码、令牌、API Key：导出时统一替换为 `REDACTED`，包括 rcon 密码、数据库密码、LLM/TTS 接口密钥、跨服通信 token 等

## 环境

- Minecraft 1.21.1，NeoForge 服务端，另加载 Paper 插件

## 说明

配置会随整合包更新变化，改动后重新导出即可。想复现服务器行为时，按 `mods.csv` 里的文件名和哈希找同一版本模组。
