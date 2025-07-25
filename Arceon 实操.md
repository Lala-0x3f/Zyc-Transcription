# **Arceon 实操指南：建筑师与体素艺术家的进阶工具**

Arceon 是一个基于 WorldEdit 的扩展插件，专为建筑师和体素艺术家设计，提供了：
- 🎨 **高级笔刷系统** - 多种专业建筑笔刷
- 🎭 **智能蒙版功能** - 精确控制编辑范围
- 🌟 **噪声图案生成** - 创造自然随机效果
- 🛠️ **专业建筑工具** - 地形、建筑、装饰工具
- 🔄 **旋转复制系统** - 快速生成对称结构
- 🎯 **材质管理工具** - 批量替换颜色和类型

## **前置要求与准备**

在开始 Arceon 建筑之旅前，您需要：
1. ✅ 安装并熟悉 **WorldEdit** 插件
2. ✅ 了解基本的 WorldEdit 命令（如 `//wand`、`//set`、`//replace` 等）
3. ✅ 拥有相应的权限节点
4. ✅ 准备一张**纸**作为 Arceon 的专用工具

## **建筑流程导向的功能分类**

### **0.1 概念设计与初期地形塑造**

在项目初期，快速生成和调整大型地形是关键。Arceon 的地形工具让您能够像雕塑家一样塑造世界。

#### **巨石笔刷 - 地形骨架构建**
**用途：** 快速创建山体、岩石群、地形起伏
**配合工具：** WorldEdit 选区、噪声蒙版
**贴合需求：** 概念阶段的地形轮廓确定

```bash
# 基础巨石生成
/ab boulder stone 15 2 20 30

# 随机化地形（关键技巧）
/ab boulder stone 10,30 1,3 15,40 20,50
```

**实用示例：** 在创建山脉时，先用大尺寸巨石（30-50格）确定主要山峰位置，再用中等尺寸（15-25格）填充山体，最后用小尺寸（5-10格）添加细节岩石。

**高级技巧：**
- `-f` 参数：让巨石自然落在地面上，避免悬空
- `-a` 参数：根据视角方向倾斜，创造动态感
- `-h` 参数：生成中空巨石，可作为洞穴入口

#### **//loft 命令 - 有机曲面生成**
**用途：** 创建流畅的地形过渡、河谷、山脊
**配合工具：** 纸（Paper）作为选择工具
**贴合需求：** 需要精确控制的地形曲线

```bash
# 创建新的路径帧
//loft frame  # 或 //lo f

# 添加路径点
//loft point  # 或 //lo p

# 生成地形
//loft set stone -d  # 堆叠到底部形成实体地形
```

**建筑流程应用：**
1. **河谷塑造：** 沿河道走向设置帧点，生成自然的河床曲线
2. **山脊线条：** 用 `-p` 参数创建锐利的山脊，用默认模式创建圆润丘陵
3. **建筑轮廓：** 为复杂建筑创建基础轮廓，如圆顶、拱形结构

### **0.2 基础设施与连接系统**

建筑项目中，道路、桥梁、拱门等基础设施的快速构建能大幅提升效率。

#### **//road 命令 - 智能道路系统**
**用途：** 自动适应地形的道路生成
**配合工具：** `//sel convex` 多边形选择
**贴合需求：** 连接建筑群、适应复杂地形

```bash
# 平地道路
//road dirt_path 5

# 山地道路（自动适应高度）
//road cobblestone 7 4

# 带噪声的自然小径
//road grass_path 3 -n
```

**实际应用场景：**
- **城市规划：** 用宽度8-12的道路连接主要建筑
- **乡村小径：** 用宽度3-5的路径，添加 `-n` 参数增加自然感
- **山地公路：** 利用高度参数让道路自动适应坡度

#### **//arch 命令 - 宏伟结构支撑**
**用途：** 快速生成桥梁、渡槽、建筑拱门
**配合工具：** 立方体或多边形选择
**贴合需求：** 跨越峡谷、装饰性拱门、结构支撑

```bash
# 基础拱门
//arch stone_bricks 8 15 6 3 60

# 统一高度的连续拱门
//arch sandstone 10 20 8 5 70 -l

# 实心基础拱门
//arch cobblestone 12 18 10 4 50 -ld
```

**设计要点：**
- **拱高百分比：** 50%为半圆，80%为高拱，30%为扁拱
- **数量控制：** 根据跨度确定拱门数量，避免过密或过疏
- **材质选择：** 石砖适合正式建筑，圆石适合乡村风格

#### **//rope 命令 - 悬挂连接艺术**
**用途：** 创建吊桥、装饰缆绳、悬挂结构
**配合工具：** 立方体选择（仅两点）
**贴合需求：** 峡谷跨越、装饰元素、动态连接

```bash
# 基础绳索
//rope chain 10 3

# 宽吊桥
//rope oak_planks 15 8

# 添加扶手后修复连接
//fixconnect
```

### **0.3 建筑主体与屋顶系统**

建筑主体完成后，屋顶往往是最具挑战性的部分。Arceon 提供了强大的屋顶生成工具。

#### **//roof 命令 - 智能屋顶生成**
**用途：** 快速生成各种形状的屋顶
**配合工具：** 立方体或多边形选择
**贴合需求：** 复杂建筑的屋顶设计、异形结构覆盖

```bash
# 标准坡屋顶
//roof red_terracotta 25 8

# 弯曲屋顶（配合convex选择）
//roof dark_oak_slab 30 12

# 带倒角的精致屋顶
//roof copper 20 6 -b
```

**屋顶设计原则：**
- **宽度参数：** 比墙体宽2-4格形成屋檐
- **高度参数：** 影响坡度，6-8适合住宅，12-15适合教堂
- **材质搭配：** 陶瓦适合地中海风格，木材适合北欧风格

### **0.4 旋转复制与对称结构**

对于需要对称或重复元素的建筑，//revolve 命令是效率神器。

#### **//revolve 命令 - 旋转复制大师**
**用途：** 创建圆形结构、对称建筑、螺旋元素
**配合工具：** WorldEdit 选区、精确定位
**贴合需求：** 圆形建筑、装饰图案、螺旋楼梯

```bash
# 基础圆形结构
//revolve 8

# 螺旋楼梯
//revolve 1000 0 720 20

# 五角星图案
//revolve 5 0 720 -p

# 连接起始点的放射结构
//revolve 100 0 360 10 -s
```

**建筑应用实例：**
- **圆形塔楼：** 设计一个扇形，用 //revolve 8 生成八边形塔
- **装饰花窗：** 创建基础图案，用 -p 参数生成多边形窗格
- **螺旋装饰：** 结合高度差创建螺旋柱或装饰元素

## **精细化阶段：蒙版与选择性编辑**

建筑进入细节阶段时，精确控制编辑范围变得至关重要。Arceon 的蒙版系统如同画家的遮罩，让您能够精确地"绘制"细节。

### **1.1 地形细化蒙版**

#### **角度蒙版 (#arcangle) - 坡度感知编辑**
**用途：** 根据地形坡度进行差异化处理
**配合工具：** //replace、//gmask
**贴合需求：** 地形分层、植被分布、风化效果

```bash
# 在缓坡（0-30度）铺设草地
//replace #arcangle[0][30] grass_block

# 在陡坡（60-90度）暴露岩石
//replace #arcangle[60][90] stone

# 平滑过渡效果
//replace #arcangle[20][40][2] coarse_dirt
```

**实际应用：**
- **山体分层：** 山顶用雪，缓坡用草，陡坡用岩石
- **河岸处理：** 缓坡种植植被，陡坡保持土壤裸露
- **建筑风化：** 在建筑的水平面添加苔藓，垂直面保持原貌

#### **环境蒙版 (#ambient) - 暴露度感知**
**用途：** 区分表面和内部方块
**配合工具：** 表面纹理、内部填充
**贴合需求：** 表面装饰、洞穴生成、建筑细节

```bash
# 为所有表面添加苔藓
//replace #ambient[1] mossy_cobblestone

# 标记完全内部的方块
//replace #ambient[4] diamond_ore
```

#### **高度蒙版 (#y & #ygradient) - 垂直分层**
**用途：** 按高度进行分层处理
**配合工具：** 地质分层、建筑楼层
**贴合需求：** 矿物分布、楼层装饰、地下结构

```bash
# 地下矿物层
//gmask "<<0"
//replace #y[10][30] iron_ore

# 高度渐变效果
//replace #ygradient[50][80] snow
```

### **1.2 精确定位蒙版**

#### **邻近蒙版 (#proximity) - 距离感知编辑**
**用途：** 在特定方块周围添加效果
**配合工具：** 边框生成、辐射效果
**贴合需求：** 建筑边框、装饰扩散、区域标记

```bash
# 为建筑添加边框（水平）
//replace #prox[diamond_block][3] black_concrete

# 立体保护层（全方向）
//replace #prox3D[beacon][5] glass
```

**注意事项：** 确保选区足够大，避免蒙版效果被截断

#### **方向蒙版 (#above/#below) - 垂直关系编辑**
**用途：** 基于垂直位置关系进行编辑
**配合工具：** 建筑延伸、装饰悬挂
**贴合需求：** 塔楼延伸、地基加固、装饰悬挂

```bash
# 向上延伸结构
//replace #above[foundation][15] tower_block

# 向下加固地基
//replace #below[building][10] reinforced_stone
```

### **1.3 材质与类型蒙版**

#### **类型蒙版 (#type) - 材质家族编辑**
**用途：** 精确控制特定材质类型
**配合工具：** 笔刷绘制、材质替换
**贴合需求：** 精细纹理、局部修改、材质升级

```bash
# 只在橡木上绘制纹理
//mask #type[oak]
//br sphere mossy_oak_planks 3

# 精确替换特定材质
//replace #type[cobblestone] stone_bricks
```

**笔刷应用技巧：** 设置类型蒙版后，笔刷只会影响指定类型的方块，让您能在复杂结构上精确"绘制"

## **自然化处理：噪声图案系统**

建筑完成后，添加自然的随机性和纹理变化能让作品更加生动。Arceon 的噪声系统是实现这一目标的利器。

### **2.1 噪声图案 (Pattern) - 直接生成**

#### **湍流噪声 (#turbulence) - 不规则斑点**
**用途：** 创建自然的斑驳纹理
**配合工具：** 地表植被、矿物分布
**贴合需求：** 地形纹理、自然过渡

```bash
# 混合植被纹理
//set #turb[3][grass_block,dirt,coarse_dirt]

# 矿物分布
//replace stone #turb[2][iron_ore,coal_ore]
```

#### **分形噪声 (#fractal) - 复杂自相似**
**用途：** 山脉纹理、复杂地形
**配合工具：** 大型地形、岩石纹理
**贴合需求：** 逼真山体、自然岩层

```bash
# 山体纹理
//replace stone #frac[4][stone,andesite,diorite]
```

#### **细胞噪声 (#cell) - 有机图案**
**用途：** 生物纹理、外星地貌
**配合工具：** 特殊建筑、艺术装饰
**贴合需求：** 独特表面、生物建筑

```bash
# 外星地表
//set #cell[2][warped_nylium,crimson_nylium][3]
```

### **2.2 噪声蒙版 (Mask) - 选择性应用**

噪声蒙版不生成新方块，而是根据噪声图案选择现有方块进行替换，更适合在已有结构上添加细节。

```bash
# 在现有墙面添加风化效果
//replace #turb[2][40] mossy_stone_bricks

# 在地面添加裂缝效果
//replace #crack[3][60] coarse_dirt

# 在建筑表面添加有机纹理
//replace #cell[2][30] weathered_copper
```

**应用策略：**
- **覆盖率控制：** 30-50%适合细节装饰，70-80%适合主要纹理
- **尺寸调节：** 小尺寸(1-2)适合细节，大尺寸(4-6)适合大面积效果
- **分层应用：** 先用大尺寸噪声确定主要区域，再用小尺寸添加细节

## **后期调整：材质管理与批量优化**

项目接近完成时，往往需要进行全局的材质调整和风格统一。Arceon 的材质管理工具让这一过程变得轻松高效。

### **3.1 颜色管理系统**

#### **//colorreplace - 色彩主题切换**
**用途：** 快速调整建筑色彩主题
**配合工具：** GUI界面选择、批量替换
**贴合需求：** 主题迭代、季节变化、风格统一

```bash
# 基础颜色替换
//colorreplace red blue

# 使用GUI界面（推荐）
//colorreplace

# 排除特殊方块
//colorreplace orange yellow -b  # 排除旗帜
//colorreplace green purple -g   # 排除釉面陶瓦
```

**实际应用场景：**
- **季节主题：** 秋季用橙色系，冬季用蓝白系，春季用绿色系
- **建筑风格：** 地中海风格用暖色调，北欧风格用冷色调
- **区域划分：** 不同功能区域用不同主色调区分

#### **色彩蒙版 (#color) - 精确色彩控制**
**用途：** 基于颜色进行精确编辑
**配合工具：** 局部调整、渐变效果
**贴合需求：** 细节调色、局部强调

```bash
# 将所有红色系方块替换为橙色系
//replace #cc[red] #cc[orange]

# 在特定颜色上添加细节
//mask #color[blue]
//br sphere light_blue_wool 2
```

### **3.2 材质类型管理**

#### **//typereplace - 材质家族转换**
**用途：** 批量更换建筑材质类型
**配合工具：** 风格转换、材质升级
**贴合需求：** 生物群系适配、建筑等级调整

```bash
# 基础材质转换
//typereplace oak birch

# 使用GUI界面
//typereplace

# 精细控制
//typereplace stone deepslate -f  # 排除栅栏和墙
//typereplace oak dark_oak -s     # 排除台阶
```

**建筑应用实例：**
- **生物群系适配：** 将温带建筑的橡木替换为热带的丛林木
- **材质升级：** 将圆石建筑升级为石砖，提升建筑等级
- **风格转换：** 将现代混凝土建筑转换为传统石材建筑

### **3.3 连接修复与细节完善**

#### **//fixconnect - 连接性方块修复**
**用途：** 修复替换后的连接问题
**配合工具：** 批量替换后的必备步骤
**贴合需求：** 保持结构完整性、视觉连续性

```bash
# 修复选区内所有连接性方块
//fixconnect

# 常见应用场景
//typereplace oak birch    # 替换栅栏材质
//fixconnect               # 修复栅栏连接
```

**重要提醒：** 每次进行大规模栅栏、玻璃板、墙体替换后，都应该运行此命令

## **实战技巧与工作流程**

### **4.1 高效工作流程**

#### **分阶段建筑法**
1. **概念阶段：** 用巨石笔刷和 //loft 确定大型轮廓
2. **结构阶段：** 用 //road、//arch、//roof 构建基础设施
3. **细化阶段：** 用蒙版系统添加细节和纹理
4. **自然化阶段：** 用噪声图案增加随机性和真实感
5. **优化阶段：** 用材质管理工具统一风格

#### **常用组合技巧**
```bash
# 地形塑造组合
/ab boulder stone 15,25 1,2 20,35 25,40 -f
//replace #arcangle[0][20] grass_block
//replace #turb[2][30] #cc[green]

# 建筑细化组合
//mask #type[stone]
//br sphere mossy_stone_bricks 3
//fixconnect

# 材质统一组合
//colorreplace red blue
//typereplace oak birch
//fixconnect
```

### **4.2 性能优化建议**

#### **选区管理**
- **合理选区：** 蒙版操作时确保选区足够大，避免效果被截断
- **分块处理：** 大型项目分区域处理，避免一次性操作过大区域
- **及时撤销：** 利用 `//undo` 和 `//redo` 进行实验和调整

#### **参数调优**
- **随机范围：** 善用 `min,max` 格式创建自然变化
- **噪声参数：** 从大尺寸开始，逐步添加小尺寸细节
- **蒙版覆盖率：** 根据需求调整，避免过度或不足

### **4.3 创意应用拓展**

#### **藤蔓笔刷的创意用法**
```bash
# 传统藤蔓
/ab vine vine 5 30 3,8

# 创意应用
/ab vine cornflower 8 25 5,12    # 花朵瀑布
/ab vine glowstone 6 20 2,6      # 发光晶体
/ab vine ice 10 40 8,15          # 冰柱效果
```

#### **//revolve 的艺术应用**
```bash
# 装饰图案
//revolve 6 -p                    # 六边形图案
//revolve 5 0 1800 -p            # 五角星螺旋

# 建筑元素
//revolve 1000 0 360 20          # 螺旋楼梯
//revolve 100 0 360 0 -s         # 放射状装饰
```

## **常见问题与解决方案**

### **Q1: 蒙版效果被截断怎么办？**
**A:** 确保选区比预期效果范围大5-10格，特别是使用邻近蒙版时。

### **Q2: 噪声效果太规律或太随机？**
**A:** 调整 `scale/zoom` 参数和 `coverage` 参数，多次实验找到合适的平衡点。

### **Q3: 替换后栅栏不连接？**
**A:** 每次材质替换后运行 `//fixconnect` 命令。

### **Q4: //revolve 生成的结构有间隙？**
**A:** 增加 `amount` 参数值，确保旋转次数足够密集。

### **Q5: 如何撤销错误操作？**
**A:** 使用 `//undo` 撤销上一步操作，`//redo` 重做操作。

