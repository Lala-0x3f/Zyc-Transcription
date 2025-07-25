# **Voxel Sniper 实操指南：建筑师与体素艺术家的雕刻利器**

Voxel Sniper（简称 VS）是一个专为 Minecraft 设计的强大笔刷工具，如同数字雕刻师的凿子，让您能够：
- 🏔️ **地形塑造** - 创建山脉、峡谷、洞穴等自然地形
- 🎨 **有机雕刻** - 精细雕刻人物、动物、植物等生物形态
- 🌍 **概念设计** - 快速构建大型地形概念和建筑轮廓
- 🔧 **细节打磨** - 为建筑添加自然的纹理和细节

## **前置要求与工具准备**

在开始 VS 雕刻之旅前，您需要：
1. ✅ 安装 **Voxel Sniper** 插件
2. ✅ 熟悉基本的 Minecraft 操作
3. ✅ 准备核心工具：**箭**🏹 和 **火药**💥
4. ✅ 可选：**WorldEdit** 插件配合使用

### **核心工具理解**

| 工具 | 图标 | 用途 | 建筑流程应用 |
|------|------|------|----------------|
| **箭** | 🏹 | **主操作工具**：添加、塑形、平滑 | 塑造主要形体，增加细节，平滑表面 |
| **火药** | 💥 | **辅助操作工具**：移除、雕刻、侵蚀 | 雕刻负空间，创建凹陷，模拟侵蚀效果 |

## **建筑流程导向的功能分类**

### **0.1 项目准备与基础设置**

在任何雕刻项目开始前，正确的设置是成功的基础。

#### **环境检查与重置**
**用途：** 确保干净的工作环境
**配合工具：** VS 状态检查
**贴合需求：** 避免之前设置的干扰

```bash
# 检查当前设置
/vs

# 重置所有笔刷（关键习惯）
/d

# 查看可用笔刷
/vs brushes      # 简称列表
/vs brusheslong  # 全名列表
```

**工作流程建议：** 每次开始新项目时，都应该执行重置命令，就像画家清洗画笔一样重要。

### **0.2 概念设计与地形骨架**

在项目初期，快速建立地形的基本轮廓和体量关系是关键。VS 的基础笔刷让您能够像雕塑家一样从粗糙的石料开始塑形。

#### **球形笔刷 - 体积构建基础**
**用途：** 快速建立基本体积和轮廓
**配合工具：** 材料设置、大小控制
**贴合需求：** 概念阶段的快速成型

```bash
# 基础球形笔刷设置
/b b            # 激活球形笔刷
/b 15           # 设置大笔刷进行粗略塑形
/v stone        # 设置材料为石头

# 执行者模式设置
/b b m          # 材料模式 - 只放置方块
/b b mm         # 材料替换材料（推荐）
```

**实际应用场景：**
- **山脉轮廓：** 用大尺寸球形笔刷（15-20）快速堆叠出山脉主体
- **建筑体量：** 为复杂建筑确定基本的体积关系
- **雕塑骨架：** 为有机体雕塑建立基础骨架结构

#### **体素笔刷 - 几何结构构建**
**用途：** 创建更具棱角的几何结构
**配合工具：** 球形笔刷的补充
**贴合需求：** 需要明确边缘的结构

```bash
/b v            # 激活体素（立方体）笔刷
/b 10           # 中等大小适合结构构建
```

**设计应用：**
- **建筑基础：** 为现代建筑或机械结构提供方正的基础
- **地形分层：** 创建明确的地质层次
- **与球形结合：** 先用体素确定硬边，再用球形软化

### **0.3 地形塑造与自然化处理**

地形的自然化是 VS 的强项，通过模拟自然侵蚀过程，让人工痕迹消失。

#### **侵蚀笔刷系统 - 自然化的核心**
**用途：** 模拟自然侵蚀，创造有机形态
**配合工具：** 不同侵蚀类型的组合
**贴合需求：** 地形自然化、有机雕塑塑形

```bash
# 基础侵蚀笔刷
/b e            # 标准侵蚀笔刷
/b 12           # 中等大小适合地形处理

# 融化侵蚀（推荐）
/b e melt       # 更自然的融化效果
/b 15-20        # 大尺寸进行宏观塑形
```

**操作技巧：**
- 🏹 **箭矢** = 侵蚀削减，创造凹陷和流线
- 💥 **火药** = 填充增长，修复过度侵蚀

**实战应用流程：**
1. **粗略塑形：** 用大尺寸融化笔刷消除所有直角
2. **细节雕刻：** 用中等尺寸添加山脊和谷地
3. **表面处理：** 用小尺寸处理细节纹理

#### **混合笔刷 - 平滑过渡大师**
**用途：** 创造平滑的表面过渡
**配合工具：** 侵蚀笔刷的后续处理
**贴合需求：** 消除生硬边界，创造自然流线

```bash
# 混合球笔刷
/b bb           # 球形混合
/b 8            # 中等大小适合大部分情况

# 混合圆盘笔刷
/b bd           # 圆盘混合，适合平面处理
```

**应用策略：**
- **有机雕塑：** 在骨架基础上用火药"拉伸"出肌肉形态
- **地形连接：** 平滑不同地形元素间的过渡
- **建筑软化：** 为硬朗的建筑边缘添加自然感

### **0.4 表面处理与材质应用**

建筑和地形的表面处理决定了最终的视觉效果和真实感。

#### **叠加笔刷 - 表面纹理专家**
**用途：** 在现有表面添加新的材质层
**配合工具：** 蒙版系统精确控制
**贴合需求：** 植被覆盖、材质分层、细节装饰

```bash
# 基础叠加笔刷
/b over         # 激活叠加笔刷
/v grass_block  # 设置覆盖材料
/b 12           # 适中大小

# 深度控制叠加
/b over d3      # 深度3的叠加，更厚的覆盖层
```

**实际应用场景：**
- **植被系统：** 在山体表面自然地铺设草地和土壤
- **建筑风化：** 为古建筑添加苔藓和风化效果
- **材质分层：** 创造地质层次感

#### **溅射笔刷 - 随机细节生成器**
**用途：** 创造自然的随机分布效果
**配合工具：** 种子和参数控制
**贴合需求：** 积雪分布、植被斑块、细节装饰

```bash
# 溅射球笔刷
/b sb mm        # 溅射球，材料替换材料
/v snow_block   # 设置为雪块
/b 8            # 中等大小

# 溅射叠加笔刷
/b sover s123 g2 r1  # 种子123，生长2，递归1
```

**设计应用：**
- **山顶积雪：** 在高海拔区域自然分布雪块
- **植被斑块：** 创造不规则的草地和花丛
- **岩石细节：** 在地形上随机分布不同类型的石块

## **有机雕塑专项技法**

VS 在有机体雕塑方面有着独特的优势，能够创造出栩栩如生的生物形态。

### **1.1 骨架构建阶段**

#### **小型球形笔刷 - 精确骨架定位**
**用途：** 建立有机体的基本骨架和关节
**配合工具：** 参考图像、比例测量
**贴合需求：** 确定姿态、比例、关节位置

```bash
# 精确骨架笔刷
/br sphere wool 2    # 使用羊毛，半径2
/b 2                 # 小尺寸精确控制
```

**骨架构建原则：**
- **脊柱优先：** 先确定主要轴线（脊柱、中轴线）
- **关节定位：** 精确标记肩、髋、肘、膝等关键关节
- **比例检查：** 从多角度检查比例关系

### **1.2 体积填充阶段**

#### **混合球笔刷 - 肌肉塑造**
**用途：** 在骨架基础上填充体积，模拟肌肉
**配合工具：** 不同大小的组合使用
**贴合需求：** 创造有机体的体积感和力量感

```bash
/b bb           # 混合球笔刷
/b 4-6          # 根据雕塑大小调整
```

**塑形技巧：**
- 💥 **火药操作：** 在骨架周围"拉伸"出肌肉形态
- 🏹 **箭矢操作：** 平滑和调整形态
- **分层构建：** 先大肌肉群，再细节肌肉

### **1.3 精细雕刻阶段**

#### **精确擦除技术 - 减法雕刻**
**用途：** 精确移除不需要的方块，如凿子雕刻
**配合工具：** 蒙版系统、小尺寸笔刷
**贴合需求：** 关节凹陷、肌肉线条、面部特征

```bash
# 精确擦除设置
/br sphere air 1     # 空气笔刷，半径1
/mask wool           # 只删除羊毛方块
```

**雕刻应用：**
- **关节塑造：** 雕刻肩膀、肘部、膝盖的自然凹陷
- **肌肉分离：** 在肌肉群之间创造分界线
- **面部特征：** 雕刻眼眶、鼻梁、嘴部轮廓

## **地形制作专项案例**

### **案例1：真实山脉制作流程**

#### **第一步：基础轮廓构建**
```bash
/d                   # 重置笔刷
/b v                 # 体素笔刷建立基础
/v stone             # 石头材料
/b 15                # 大笔刷建立主体
```

**操作流程：**
1. 用箭矢堆叠大型立方体群，确定山脉走向
2. 切换到中等笔刷（/b 8-10）添加次级山峰
3. 建立山脉的基本高度层次

#### **第二步：侵蚀自然化**
```bash
/b e melt            # 融化侵蚀笔刷
/b 15-20             # 大尺寸宏观塑形
```

**塑形策略：**
1. 用箭矢对立方体进行多次"融化"
2. 消除所有直角和平面
3. 用火药修复过度侵蚀的区域

#### **第三步：细节层次添加**
```bash
/b e lift            # 提升侵蚀笔刷
/b 6-8               # 中等大小处理细节
```

**细节处理：**
1. 创造山脊和谷地的细节变化
2. 添加岩石露头和悬崖面
3. 用混合笔刷进行最终平滑

#### **第四步：材质分层**
```bash
# 使用WorldEdit进行材质替换
//replace stone stone,andesite,diorite,gravel
```

#### **第五步：植被和积雪**
```bash
# 植被覆盖
/b over d3           # 叠加笔刷
/v dirt              # 土壤层
/b 15

# 积雪效果
/b sb mm             # 溅射球笔刷
/v snow_block        # 雪块
/b 6                 # 在山峰添加积雪
```

### **案例2：洞穴系统雕刻**

#### **洞穴网络规划**
```bash
/b b                 # 球形笔刷
/b 6                 # 中小型洞室
```

**挖掘策略：**
1. 用火药在山体内部挖掘主要洞室
2. 用小笔刷（/b 3）连接洞室形成通道
3. 创造不同大小的空间层次

#### **自然化洞穴形状**
```bash
/b re                # 随机侵蚀笔刷
/b 4                 # 小笔刷细节处理
```

**细节雕刻：**
1. 用随机侵蚀打破规整的球形
2. 用提升侵蚀创造钟乳石和石笋
3. 添加不规则的岩石纹理

## **效率提升与工作流程**

### **笔刷组合策略**

#### **地形制作标准流程**
1. **体素笔刷** → 建立基础轮廓和体量
2. **融化侵蚀** → 自然化塑形，消除人工痕迹
3. **混合球笔刷** → 整体平滑和过渡
4. **材质替换** → 使用WorldEdit进行大面积材质变化
5. **叠加/溅射笔刷** → 添加植被、积雪等细节

#### **有机雕塑标准流程**
1. **小球形笔刷** → 精确构建骨架和关节
2. **混合球笔刷** → 填充体积，塑造肌肉
3. **精确擦除** → 减法雕刻，创造细节
4. **手工平滑** → 最终的精细调整
5. **材质应用** → 添加纹理和颜色细节

### **常见问题与解决方案**

#### **Q1: 地形过于平滑缺乏细节？**
**解决方案：**
- 使用随机侵蚀笔刷（/b re）增加变化
- 减少混合球笔刷的使用频率
- 用小尺寸球形笔刷手动添加岩石细节

#### **Q2: 有机雕塑比例不协调？**
**解决方案：**
- 在骨架阶段多花时间检查比例
- 使用参考图像进行对比
- 从多个角度（360度）观察作品

#### **Q3: 笔刷效果不如预期？**
**解决方案：**
- 检查执行者模式设置（/b [笔刷] [模式]）
- 确认材料设置（/v [材料]）
- 重置笔刷后重新设置（/d）

#### **Q4: 材质过渡生硬？**
**解决方案：**
- 在材质交界处使用混合球笔刷
- 使用溅射叠加创造渐变效果
- 调整叠加笔刷的深度参数

---

**结语：** Voxel Sniper 是体素艺术家手中的数字凿子，它不仅能够塑造宏伟的地形，更能雕刻出栩栩如生的有机形态。掌握这些技法后，您将能够像真正的雕塑大师一样，从粗糙的方块中雕琢出令人惊叹的艺术作品。记住，最好的雕塑来自于对工具的熟练掌握和对自然形态的深入观察。
