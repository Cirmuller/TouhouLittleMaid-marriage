# Touhou Little Maid: 婚姻扩展（NeoForge 1.21.1）

本模组是车万女仆（Touhou Little Maid）的附属扩展，核心内容包括：
结婚求婚、同床事件、怀孕分娩、子代女仆成长，以及子代学习/探险工作系统。

![模组预览](./五彩花束.png)

- GitHub: https://github.com/YunChenqwq/TouhouLittleMaid-marriage
- Minecraft: 1.21.1
- 加载器: NeoForge 21.1.x
- Java: 21
- 前置模组: Touhou Little Maid（NeoForge 1.21.1）

## 主要功能

### 1）求婚 / 结婚 / 同床流程
- 使用 `proposal_ring` 向女仆求婚。
- 结婚后可使用 `yes_pillow` 触发节奏结算面板与同床流程。
- 同床后可进入怀孕流程，后续满足条件会分娩。

### 2）子代女仆
- 子代女仆会经历成长阶段，最终成长为成年女仆。
- 支持模型继承（含 YSM 相关数据继承）。
- 魂符收回与再次召唤时，尽量保持子代状态一致性。

### 3）子代工作（学习 / 探险）
- 在女仆任务面板中切换工作状态。
- 材料消耗优先读取主手。
- 药剂学/战术学等不可堆叠材料可从背包回退消耗。
- 近郊探险材料为 `木棍`，单次固定产出 2 件物品。

### 4）好感度系统
- 子代女仆默认有基础好感。
- 工作会消耗好感，空闲休息可恢复好感。
- 好感过低会锁定行动，恢复后可继续工作。

### 5）节奏结算面板
- 使用 `yes_pillow` 后进入 HUD 节奏面板进行结算。
- 支持头像切换、逐字机对话、命中判定与连击逻辑。
- 支持在配置中调整节奏判定键。

### 6）怀孕与调试显示
- 分娩判定按配置天数精确换算为 tick 计算。
- 可在配置中开启“分娩倒计时调试显示”，左上角显示秒级倒计时。

## 构建与运行

```powershell
./gradlew.bat build
./gradlew.bat runClient
```

如果本机没有 Java，请先将 `JAVA_HOME` 指向 JDK 21。

## 快速测试指令

```mcfunction
/give @p maidmarriage:proposal_ring
/give @p maidmarriage:yes_pillow
/give @p maidmarriage:longing_tester
```
