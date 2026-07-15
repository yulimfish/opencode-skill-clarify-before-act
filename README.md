# opencode-skill-clarify-before-act

> opencode 技能：在真的存在分支决策的任务上，用**一条**确认消息卡住手，让用户一次拍板 —— 而不是眼睁睁看着 agent 一路瞎猜。

隶属 [`opencode-codex-kit`](https://github.com/Yulimfish/opencode-codex-kit)。

## 什么时候触发

在正式动手前，符合**任一**条件就加载本技能：

- 有多条可行路径，且存在非平凡的取舍（架构、破坏性变更、数据丢失风险）。
- 验收标准模糊，猜错会浪费 >5 分钟。
- 破坏性动作超出 git 追踪范围（`rm -rf`、`git reset --hard`、force-push、drop DB）。

一目了然的任务**跳过**。这个技能是为了防止空转，不是给自己加摩擦。

## 安装

```bash
mkdir -p ~/.config/opencode/skills
git clone https://github.com/Yulimfish/opencode-skill-clarify-before-act.git \
  ~/.config/opencode/skills/clarify-before-act
```

重启 opencode，技能按名字自动被发现。

## 许可

MIT © Yulimfish
