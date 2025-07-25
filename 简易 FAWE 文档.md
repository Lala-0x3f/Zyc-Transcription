# 简易 FAWE 文档

FastAsyncWorldEdit (FAWE) 简易指南

FastAsyncWorldEdit (FAWE) 是 WorldEdit 的增强版本，它在速度和内存使用方面进行了显著优化，并提供了更多功能。如果您的服务器使用依赖 WorldEdit 的插件，安装 FAWE 可以大幅提升它们的性能。

## FAWE主要特点

性能优化：显著提升速度和内存效率。

更多功能：包含 WorldEdit 的所有功能，并增添了多种额外特性。

兼容性：与依赖 WorldEdit 的其他插件完全兼容。

## FAWE命令语法

FAWE 命令通常以双斜杠 // 开头。

<arg>：必需参数

<arg1|arg2>：多个参数选项

<arg=value>：默认或建议值

- a：命令旗标（例如，//<command> -a [flag-value]）

需要更多信息？在游戏内使用 //help [类别|命令]。

## FAWE主要命令类别

FAWE 命令分为以下类别，方便用户进行各种操作：

### FAWE世界编辑命令 (World Edit Commands)：用于更新、信息查询、调试和帮助。

//we version：获取 WorldEdit/FAWE 版本。

//cancel：取消当前操作。

### FAWE实用工具命令 (Utility Commands)：各种实用工具。

//fixwater <半径>：修复水流。

//fill <模式> <半径> [深度] [方向]：填充洞穴。

//drain <半径>：排干水域。

//butcher [半径]：清除附近生物。

### FAWE区域命令 (Region Commands)：操作选定区域。

//set <模式>：在选区内设置所有方块。

//replace [来自-掩码] <到-模式>：替换选区内的方块。

//stack [数量] [方向]：复制并堆叠选区内容。

//move [数量] [方向] [保留ID]：移动选区内容。

//naturalize：将区域自然化（顶部三层为泥土，下方为岩石）。

### FAWE选区命令 (Selection Commands)：修改选区点、模式或查看信息。

//wand：获取选择工具。

//pos1 [坐标], //pos2 [坐标]：设置位置点1和点2。

//expand <数量> [反向数量] <方向>：扩大选区。

//contract <数量> [反向数量] [方向]：缩小选区。

//sel [类型]：选择区域选择器类型（如 cuboid, poly, ellipsoid）。

//size：获取选区信息。

### FAWE历史命令 (History Commands)：用于撤销、重做和清除历史。

//undo [次数]：撤销上一个操作。

//redo [次数]：重做上一个操作。

//clearhistory：清除历史记录。

### FAWE剪贴板命令 (Clipboard Commands)：复制和粘贴方块。

//copy：复制选区到剪贴板。

//cut [保留ID]：剪切选区到剪贴板。

//paste：粘贴剪贴板内容。

//rotate <Y轴> [<X轴>] [<Z轴>]：旋转剪贴板内容。

//flip [<方向>]：翻转剪贴板内容。

### FAWE生成命令 (Generation Commands)：创建结构和地形。

//sphere <模式> <半径>：生成实心球体。

//cyl <模式> <半径> [高度]：生成圆柱体。

//pyramid <模式> <大小>：生成实心金字塔。

### FAWE生物群系命令 (Biome Commands)：修改、列出和检查生物群系。

//setbiome <生物群系>：设置区域的生物群系。

/biomelist：列出所有可用的生物群系。

### FAWE笔刷命令 (Brush Commands)：远程建造和绘制。

//brush sphere <模式> [半径]：创建球体笔刷。

//brush smooth [大小] [迭代次数]：平滑地形。

//brush clipboard：使用剪贴板内容作为笔刷。

掩码 (Masks)：决定方块是否可以放置。

示例：>[stone,dirt],#light[0][5],$jungle（在光照等级0-5的石头、泥土或丛林生物群系中，且上方有方块）。

模式 (Patterns)：决定放置什么方块。

示例：#surfacespread[10][#existing],andesite（在现有方块的表面随机扩散安山岩）。

变换 (Transforms)：修改方块的放置方式。

#rotate <rotateX> <rotateY> <rotateZ>：旋转所有变化。

#scale <dx> <dy> <dz>：缩放所有变化。

---

好的，这是为『筑·缘』服务器新玩家精简和优化的地皮系统文档。

我移除了所有面向开发者的API文档、复杂的权限节点信息和不常用的命令，并简化了命令格式，使其更易于新玩家理解和使用。

---
