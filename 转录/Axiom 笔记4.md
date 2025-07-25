当你选中**热键栏 1-9 槽位**的任意物品时，按住 `Left Alt` 键，会弹出一个强大的上下文菜单。这里集合了 Axiom 的“超能力”！

### 左侧核心功能：突破原版限制

-   **无限距离 (Infinite Reach)**：开启后，你可以无视距离限制，直接放置、破坏或选取远处的方块。
    *   **场景设计价值**：在大型场景中快速定位和修改远处的细节，无需频繁飞行或搭建脚手架。
-   **修补工具 (Tinker)**：超级版“调试棒”！右键点击方块，可以循环改变其状态（如楼梯朝向、墙的连接方式、剥皮原木等）。
    *   **场景设计价值**：精细调整方块细节，实现更复杂的纹理和连接效果，无需担心方块更新导致结构崩溃。
-   **无更新 (No Updates)** & **强制放置 (Force Place)**：
    -   **无更新**：放置或破坏方块时，不会触发周围方块的更新（比如沙子不会下落，水不会流动）。
    -   **强制放置**：允许你将方块放置在通常无法放置的地方（比如在空中放树苗，或在不规则表面放置方块）。
    *   **场景设计价值**：这两个功能结合使用，可以创造出很多原版无法实现的“魔法”建筑效果，例如悬浮的沙子、不规则的植物生长点，为超现实或幻想场景提供无限可能。
-   **推土机 (Bulldozer)**：开启后，按住左键可以超快速地破坏方块。
    *   **场景设计价值**：快速清理大面积区域，为新建筑腾出空间，或高效地进行地形改造。
-   **增强飞行 (Enhanced Flight)**：更精准的飞行模式，没有惯性，指哪飞哪。
    *   **场景设计价值**：在复杂或狭小的空间内进行精细操作，提高建造效率和舒适度。
-   **替换模式 (Replace Mode)**：
    -   **开启后**：`左键`破坏方块，`右键`则会将你点击的方块**替换**成你手上拿着的方块。
    *   **场景设计价值**：大面积更换建筑材料时，能够快速迭代设计，尝试不同的材质组合。

### 右侧实用工具：便捷辅助

-   **飞行速度调节**：拖动滑块，最高可达10倍飞行速度，让你在大型地图中穿梭自如。
-   **垃圾桶**：将不需要的物品拖入即可销毁。
-   **游戏模式切换**：快速在创造、生存、冒险和观察者模式间切换。

## 核心功能一：建造者工具 (Builder Tools) - 快速搭建与结构调整

这是 Axiom 最直观、最适合新手的部分。所有操作都在游戏内完成，所见即所得，非常适合快速构建和修改大型结构。

#### 激活工具箱

选择**第 10 个热键栏槽位**（按键盘 `0` 键）。现在，按住 `Left Alt` 键并滚动**鼠标滚轮**，即可在不同的建造工具之间切换。

#### 关键操作逻辑（必须掌握！）

Axiom 的大部分工具都遵循这套逻辑，学会它就等于学会了 80% 的基础操作：

-   **设置选区起点**：`鼠标左键` 点击方块。
-   **设置选区终点**：`鼠标右键` 点击方块，形成一个长方体选区。
-   **扩展不规则选区**：`鼠标中键` 点击任意方块，将其纳入选区。
-   **执行/预览操作**：通常是**滚动鼠标滚轮**。
-   **确认操作**：`鼠标右键`。
-   **取消操作**：`鼠标左键`。
-   **撤销/重做**：**`Ctrl + Z`** 撤销，**`Ctrl + Y`** 重做。这是你的“后悔药”，大胆尝试吧！

#### 常用工具详解

1.  **移动 (Move)** & **克隆 (Clone)**
    -   **功能**：移动或复制选中的建筑。克隆会保留原建筑。
    -   **操作**：选区后，滚动滚轮移动预览，`右键`确认。
    -   **实用技巧**：克隆后可连续`右键`粘贴多次。移动时按 `Ctrl + R` 旋转，`Ctrl + F` 翻转。
    *   **场景设计价值**：快速复制重复元素（如柱子、窗户），或将已建好的模块移动到最终位置，大大提高大型建筑的效率。旋转和翻转功能则能轻松实现对称或镜像效果。

2.  **堆叠 (Stack)**
    -   **功能**：像乐高一样，沿着你面向的方向无缝拼接复制品。
    *   **场景设计价值**：快速建造长城、高楼、地板等重复性结构，尤其适用于有规律的阵列布局。

3.  **挤出 (Extrude)**
    -   **功能**：延伸一个平面。`右键`向外延伸，`左键`向内缩减。
    *   **场景设计价值**：加厚墙壁、延伸平台、快速塑造建筑的体量感。

4.  **擦除 (Erase)**
    -   **功能**：安全地删除方块。
    -   **操作**：创建选区后，按下 `Delete` 键。
    *   **场景设计价值**：可精确预览删除范围，防止误操作，在进行复杂雕刻或清理工作时尤为重要。

---

## 核心功能二：编辑器模式 (Editor Mode) - 你的数字画板

当你完成了建筑的“骨架”，就该为它“上色”了。编辑器模式是 Axiom 实现复杂材质、渐变和光影的终极武器。

#### 进入编辑器

按下 `Right Shift` 键，即可进入/退出编辑器模式。这是一个独立于游戏的 3D 视图，让你能更自由地观察和操作。

#### 绘画与材质入门 (Easy)

1.  **快速替换 (Active Block Drag & Drop)**：
    -   在右侧的 **Active Block** 窗口选择一个新方块（如石头）。
    -   直接将这个方块**拖拽**到建筑上你想替换的旧方块（如钻石块）上。
    -   所有与该钻石块**相连**的钻石块都会被替换成石头。
    *   **场景设计价值**：最快、最简单的换材质方法，适合快速尝试不同配色方案，或统一大面积区域的材质。

2.  **魔术选择 (Magic Select)**
    -   在左侧工具栏选择**魔术棒**图标。
    -   现在你可以`右键`点击不同种类、不相连的方块（如屋顶和地基），将它们同时选中。
    -   选中后，再从 **Active Block** 拖拽方块，可以一次性替换所有选中的部分。
    *   **场景设计价值**：精确地选择和替换场景中分散的特定材质，例如将所有灯具替换成新的光源，或统一不同区域的道路材质。

#### 渐变与纹理进阶 (Medium)

1.  **渐变画笔 (Painter - Gradient Mode)**
    -   选择**画笔工具**，在 **Tool Options** 中将 **Mode** 从 `Active Block` 改为 `Gradient`。
    -   添加你想要的渐变方块列表（如从深色到浅色的铜块）。
    -   现在，用画笔在建筑上涂抹，就能画出自然的渐变效果！
    -   **关键参数**：
        -   **Interpolation (插值)**：`Linear` 或 `Bezier` 模式会增加噪点，让渐变过渡更自然。
        -   **Merge Strokes (合并笔触)**：勾选后，多次涂抹会融合成一个平滑的整体。
    *   **场景设计价值**：为墙壁、地面或大型结构添加平滑自然的颜色过渡，模拟光影、磨损或生物群系变化，提升视觉层次感。

2.  **渐变绘制器 (Gradient Painter)**
    -   这是一个更精确的渐变工具。
    -   **操作**：`右键`点击设置渐变**起点**，再次`右键`设置**终点**，此时按住并拖动鼠标即可绘制。
    *   **场景设计价值**：制作大范围、方向性强的渐变，如墙壁从下到上的颜色变化，或模拟水体深度的渐变效果。

#### 材质与光影大师 (Hard)

1.  **噪点画笔 (Noise Painter) - 创造纹理**
    -   **功能**：使用噪点图案来混合多种方块，创造复杂的纹理。
    -   **核心技巧：Anisotropic (各向异性)**
        -   勾选 `Anisotropic`，你可以分别调整 X, Y, Z 轴的 **Scale (缩放)**。
        -   **拉伸 Y 轴**：可以做出**流挂、风化**的效果，模拟水痕、藤蔓或自然侵蚀。
        -   **拉伸 X/Z 轴**：可以模拟**砖墙**或**木板**的纹理，增加建筑的细节和真实感。
        *   **场景设计价值**：这是创造逼真材质的**关键**！通过调整噪点模式和各向异性，你可以为岩石添加裂缝、为墙壁增加风化痕迹，或为地面铺设不规则的植被，打破方块的规整感，赋予场景生命力。

2.  **自动着色 (Autoshade) - 一键添加光影**
    -   **功能**：根据设定的光源，自动为你的建筑添加明暗关系，瞬间提升立体感。
    -   **操作流程**：
        1.  用**魔术选择**选中需要着色的区域。
        2.  在顶部菜单栏选择 `Operations` -> `Autoshade`。
        3.  在弹出的窗口中，设置你的**调色板**（Palette Options -> Type -> Custom），选择用于着色的方块。
        4.  设置光源方向（`From` -> `Custom Positions` 或 `Sun Angle`）。
        5.  点击 `Autoshade` 按钮！
    -   **实用技巧**：
        -   **Dither (抖动)**：数值越低，阴影过渡越平滑；越高，噪点越多。通常 `0.05` 左右效果不错，用于模拟柔和的光影。
        -   **Global Illumination (全局光照)**：调整整体的明暗度。
    *   **场景设计价值**：无需手动放置大量方块来模拟光影，Autoshade 能快速为你的建筑添加深度和真实感，使其在不同光照下呈现出更丰富的细节。

#### 终极技巧：颜色场 (Generate Colour Field) - 发现完美配色

不知道用哪些方块做渐变或调色板？让 Axiom 帮你！

1.  在一个空旷区域，用**方框选择工具**框选一个大空间。
2.  进入 `Operations` -> `Generate Colour Field`。
3.  Axiom 会将游戏里所有方块按颜色排列在这个空间里，形成一个巨大的 3D 调色板。
4.  现在，使用**尺子工具 (Ruler)**，在颜色场中从一个方块`右键`拉到另一个方块，尺子路径上的所有方块就是一组完美的渐变！
5.  用`鼠标中键`依次拾取这些方块，即可创建你的自定义渐变调色板。
*   **场景设计价值**：解决“选择困难症”！Axiom 帮你直观地探索 Minecraft 中所有方块的颜色关系，轻松找到和谐的渐变组合，为你的建筑和场景提供无限的配色灵感。

---

## IV. 案例分析：Axiom 在场景设计中的应用

### 🌳 案例一：快速“生长”有机树叶（视频 0:00 - 0:50）

视频中展示了如何高效地为树木创建自然、蓬松的树叶效果。这结合了地形塑造、形状工具和噪点画笔。

1.  **基础地形塑造 (Elevation Tool)**：
    *   **技巧**：使用**Elevation Tool**（通常是画笔工具下的一个模式），通过调整半径和Y轴限制，快速绘制出层层叠叠的粗略地形轮廓。
    *   **设计思考**：这是为树叶提供“骨架”的第一步。即使是粗糙的轮廓，也能为后续的精细化提供指导，确保树叶的整体形态自然。

2.  **创建基础叶团 (Shape Tool + Supersphere + Metaball)**：
    *   **技巧**：选择**Shape Tool**，将形状设为`Supersphere`（超级球体），并勾选`Metaball`修改器。选择一种**占位符方块**（如绿羊毛）。通过点击和调整，生成不同大小的“叶团”基础形状。
    *   **设计思考**：Metaball 效果能让多个球体平滑地融合在一起，形成有机、流动的形状，避免了传统方块堆砌的僵硬感。占位符方块则方便后续替换。

3.  **叶团的复制与调整 (Copy/Paste, Unlock Rotation, Scale)**：
    *   **技巧**：选中这些叶团，使用**Copy/Paste**功能。粘贴时，勾选`Unlock Rotation`，并使用`Rotate/Scale`功能调整每个叶团的朝向、大小和位置。
    *   **设计思考**：通过旋转和缩放，打破了叶团的重复性，使其看起来更自然、随机。这是赋予树木独特形态的关键一步。

4.  **精细化叶片纹理 (Noise Painter + Tool Mask)**：
    *   **技巧**：
        1.  切换到**Noise Painter**工具，选择`Simplex`噪点类型，并设置一个较小的`Scale`（如1）。
        2.  **核心：应用工具遮罩 (Tool Mask)**：在“Tool Masks”面板中，添加一个`AND`条件。
            *   第一个条件：`Block = Air` (确保只在空气中放置方块)。
            *   第二个条件：`Near = [你的小分支方块]`，并设置一个`Radius`（例如4或5）。这个条件确保只在小分支周围的空气中生成叶片。
        3.  选择最终的叶片方块（如橡树叶），然后直接在树的周围涂抹。
    *   **设计思考**：
        *   **Tool Mask**是这里的魔法！它让噪点画笔只作用于树枝末端的空气区域，避免了叶片在树干内部或远离树枝的地方生成，极大地提高了效率和准确性。
        *   **Noise Painter**则负责生成不规则的叶片分布，模拟真实树叶的疏密和层次感，避免了方块堆砌的平坦感。通过调整`Scale`，可以控制叶片的“蓬松度”或“紧凑度”。

### 🧱 案例二：无损材质替换与方向保持（视频 0:00 - 0:50）

视频中展示了如何将一个由橡木（Oak）制成的复杂结构，快速且完美地替换为桦木（Birch）材质，同时保留了所有方块的朝向和状态。

1.  **创建复杂结构**：
    *   **技巧**：使用各种橡木方块（如橡木门、橡木栅栏、橡木楼梯、橡木台阶等）搭建一个包含多种状态和朝向的结构。
    *   **设计思考**：在建筑设计中，我们经常需要尝试不同的材质组合。手动替换每一个方块并调整其朝向是非常耗时且容易出错的。

2.  **整体选择 (Box Select)**：
    *   **技巧**：使用**Box Select**工具（通常是鼠标左键和右键框选），将整个结构选中。
    *   **设计思考**：确保所有需要替换的方块都在选区内。

3.  **类型替换 (Type Replace) 操作**：
    *   **技巧**：在顶部菜单栏选择 `Operations` -> `Type Replace`。
    *   在弹出的窗口中：
        *   `From`：选择你想要替换的原始方块类型（例如，选择一个橡木楼梯，Axiom会自动识别所有橡木方块）。
        *   `To`：选择你想要替换成的新方块类型（例如，选择一个桦木楼梯）。
        *   点击`Replace`。
    *   **设计思考**：这是 Axiom 最强大的“魔术”之一。`Type Replace`不仅替换了方块类型，更重要的是它**保留了原始方块的所有状态和朝向**。这意味着你的楼梯、门、活板门等特殊方块在替换后依然保持原有的方向和功能，极大地加速了材质迭代和设计调整的流程。
