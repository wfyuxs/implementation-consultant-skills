# 实施顾问 Skills

面向 SAP / ERP 实施顾问的 AI Agent 技能集合，用于项目规划、业务分析、交付检查与上线准备。

## 技能目录

| Skill | 用途 |
|---|---|
| [asap-implementation](skills/asap-implementation/SKILL.md) | 基于经典 ASAP 五阶段编制实施计划、业务蓝图、阶段验收、切换和运维交接方案 |

## 使用方式

1. 通过仓库的 **Code → Download ZIP** 下载并解压，或使用 Git 克隆本仓库。
2. 找到 `skills/asap-implementation/`，保留整个文件夹及其中的 `references/`、`agents/` 文件。
3. 将完整技能文件夹放入你使用的 AI 工具所支持的技能目录，按照该工具的说明加载。也可以直接阅读 SKILL.md 和配套模板。

调用示例：

```text
使用 $asap-implementation，为预计三个月上线的 ERP 项目制定实施计划，
明确交付物、责任人、依赖和验收标准。资料不足的部分请标明假设。
```

更多示例：

- 根据业务调研记录整理业务蓝图，列出流程、规则、例外、数据责任和验收场景。
- 检查当前项目是否具备进入最终准备阶段的条件，给出证据缺口与关闭行动。
- 编制上线切换计划，包含依赖、验证、中止条件以及回退或恢复安排。

## 仓库结构

```text
skills/
└── asap-implementation/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
        ├── delivery-templates.md
        ├── phase-gates.md
        └── sources.md
```

后续新增技能放入独立的 `skills/<skill-name>/` 目录，并更新技能目录。

## 方法依据

当前 ASAP Skill 采用经典五阶段：项目准备、业务蓝图、实现、最终准备、上线与支持。它是用于实际交付的方法裁剪，不是 SAP 官方认证模板，也不默认替代 SAP Activate。资料来源见 [方法依据](skills/asap-implementation/references/sources.md)。

AI 输出用于辅助实施顾问工作；正式验收、风险接受与上线决定仍由项目授权角色负责。
