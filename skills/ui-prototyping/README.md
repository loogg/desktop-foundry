# UI 原型设计（ui-prototyping）

帮助 Agent 组织和表达 UI 设计成果：按内容划分 Page、呈现产品画面、表达复杂组件，以及在需要的对象旁标注说明。配合所选平台和设计插件使用。

[SKILL.md](SKILL.md) 包含可直接执行的约定；[组织与标注示例](references/organization-and-expression.md) 仅在需要具体例子时读取，无需复制进提示词。

## 在 Figma 中使用

基础搭配为 **ui-prototyping + Figma + design-system-ops**。发送前选中 Skill 并附上对应插件，替换模板中的方括号；选填行可以删除。

需要额外设计支持时，再附上 **Taste** 或 **Impeccable**，并将模板首句中的“Figma 和 design-system-ops”替换为“Figma、design-system-ops 和 Taste”或“Figma、design-system-ops 和 Impeccable”。插件中的能力按本次任务选用。

### 从需求制作

```text
使用 $ui-prototyping，配合 Figma 和 design-system-ops 插件，根据以下需求制作用于后续开发的 Figma UI 原型。

需求：[需求描述或文档]
目标位置：[Figma 文件或文件夹链接]
补充约束（选填）：[使用场景、风格参考、已有资源等]

直接完成设计，提供可编辑的 Figma 文件链接；制作了交互演示时附上入口。
```

### 完善已有设计

```text
使用 $ui-prototyping，配合 Figma 和 design-system-ops 插件，完善以下 Figma UI 原型。

现有设计：[文件或节点链接]
本次改动：[需求或问题]
补充约束（选填）：[需要保留的内容、风格参考等]

沿用现有资源和适用约定，在本次范围内完成修改，提供更新后的文件链接。
```

## 使用其他平台

将所用平台的插件或工具附到消息中，填入实际名称即可。

```text
使用 $ui-prototyping，配合 [平台的插件或工具名称]，在 [平台名称] 中完成以下 UI 原型设计或修改。

需求或改动：[需求描述或文档]
目标位置：[现有项目、文件或保存位置]
补充约束（选填）：[使用场景、风格参考、已有资源等]

将 Skill 中的 Figma 术语按设计意图对应到本平台，完成后提供可继续编辑的项目入口。
```
