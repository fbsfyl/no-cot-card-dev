# no-cot-card-dev

A reusable methodology for building SillyTavern character cards and world books against models whose chain of thought is not exposed.

面向无思考（隐藏推理）模型的 SillyTavern 角色卡 / 世界书开发方法论。

## 为什么需要它

这类模型只有一次输出机会，所有判断都要在正文里完成。给 DeepSeek 这类可开思考的模型写的提示词，直接搬过去会失效：

- 「在动笔前先判断」会漏进正文，变成旁白里的心理描写。
- 「克制」「疏离」只是调概率，不产生行为。
- 「不要撤销玩家的动作」拦不住「指尖一勾把你拽了回来」。

这份 skill 把可复用的部分提炼成流程，不绑定具体题材、角色卡或模型。

## 覆盖内容

1. **先分类**：边界问题改规则，动机问题改设定，能力问题换模型。三类混改是多数返工的来源。
2. **可数指标**：用段数、次数、动作清单替代字数区间和气质词。
3. **写属性不写条件**：条件句会让行为消失，属性句会让行为泛化。
4. **位置决定权重**：硬约束放在最靠近生成点的位置，但它只在规则本身够硬时有效。
5. **删优先于加**：先问现有哪条规则本该覆盖，再决定是否新增。
6. **条目单一职责**：一个世界书条目只定义一个东西，不在 A 里解释 B。
7. **测试纪律**：一次一处、小样本不比较、通读全文判越界、先验证工具。

## 安装

项目级：

```text
<your-project>/.trae/skills/no-cot-card-dev/SKILL.md
```

全局（CN 环境）：

```text
~/.trae-cn/skills/no-cot-card-dev/SKILL.md
```

SKILL.md 已包含 frontmatter，复制目录即可，不需要其它依赖。

## 适用边界

规则来自一张修仙卡、两个 RP 模型的实测，属于启发式而非保证。跨批次漂移常常大于版本差异，任何结论都建议自己复测。

## License

MIT
