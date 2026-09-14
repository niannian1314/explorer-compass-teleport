# 探险家指南针传送扩展 (Explorer's Compass Teleport)

**modId**: `explorer_compass_teleport_mod_1785563673`  
**版本**: 1.1.0  
**加载器**: Minecraft Forge 47.4.10+  
**MC 版本**: 1.20.1 – 1.21  
**作者**: 2046820954@qq.com  
**许可证**: All Rights Reserved

## 功能说明

这是一个 **Explorer's Compass（探险家指南针）附属模组**，在原版指南针定位结构的基础上加入了**直接传送**能力，并新增一个可输入任意坐标传送的道具。

### 新增物品

#### 1. 探险家指南针传送 (Explorer's Compass Teleport)
- **合成**：指南针居中，四周围 4 颗末影珍珠（十字形）。
- **用法**：选定要找的结构后使用，**直接把玩家传送到该结构附近**。
- **安全/距离校验**：
  - 距离过远会拒绝并提示「The structure is too far away…」；
  - 找不到安全落点会提示「Cannot find a safe spot…」；
  - 传送成功提示「Teleported near the structure!」。

#### 2. 坐标传送 (Coordinate Teleport)
- **合成**：黑曜石围成菱形，中心一颗末影之眼。
- **用法**：使用后弹出坐标输入界面（Enter Coordinates），输入 X/Y/Z 后点 Teleport 传送。
- 带 Y 轴越界、非法坐标校验。

### 技术要点

- 通过 Mixin `MixinItemUtils` 注入探险家指南针的物品逻辑；
- 自定义网络包 `TeleportRequestPacket` 处理服务端传送；
- 自定义 GUI 屏幕 `CoordinateInputScreen`；
- 新物品加入 `minecraft:compasses` 标签。

## 依赖

- Forge `[47.4.10,)`
- Minecraft `[1.20.1, 1.21)`
- **Explorer's Compass** (`explorerscompass`)（必需，AFTER）

## 仓库内容说明

本仓库只包含**文本资源**（`mods.toml`、英文语言文件、合成配方、指南针标签、Mixin/Refmap 配置、物品模型）。`.class` 字节码与物品贴图为二进制未上传。

请在 GitHub 网页 **Add file → Upload files** 拖拽完整 `.jar`，或在 **Releases** 中发布。
