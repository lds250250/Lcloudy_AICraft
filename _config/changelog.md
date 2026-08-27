# 变更日志

## 2026-08-27

- 【升版】`文本处理车间/skill_v1.0.md` → `文本处理车间/结构化重塑_skill_v1.1.md`：文件名引入技能名前缀，标题同步升版；文件内历史注释同步改为 `结构化重塑_prompt_v0.1.md`
- 【对齐】结构扁平化：车间直接存放技能文件、取消项目子层（随用户手动调整确认）。`_config/global_rules.md` 命名规则改为「车间直含技能文件 + `{技能名}_prompt_vX.X.md` / `{技能名}_skill_vX.X.md`」，注意事项补充「单个技能只有一个活跃文件」；`README.md` 目录结构/场景一/二/三/当前状态/下一步全面切换为新命名；`_prompts/write_skill.md`、`_prompts/README.md` 产出文件名统一为 `{技能名}_skill_vX.X.md`
- 【新增】`_config/global_rules.md`、`README.md`：新增「Prompt 与 Skill 的判定标准」——以可调用性（loader）、行为契约（spec）、可验收性（eval）三条标准定义 prompt → skill 的升级门槛；`examples.md` 列为加分项
- 【修复】`文本处理车间/结构化重塑/_skill_evolution/eval.md`、`skill_loader.md`、`examples.md`：合格线口径统一为 **≥ 32/45**（原「18/25」与满分 45 自相矛盾）
- 【修复】`文本处理车间/结构化重塑/prompt_v0.1.md`：三处「待处理文本」占位符显式化为 `{{待处理原文}}`
- 【修复】`文本处理车间/结构化重塑/_skill_evolution/spec.md`：§4 明确 prompt 模式有要求时文末「认知框架图」以 prompt 为准；§3 明确段内结构与模式选择的分工
- 【删除】`文本处理车间/结构化重塑/_skill_evolution/examples.md`、`_prompts/write_examples.md`：examples 从默认体系中移除，降级为框架层面的可选加分项
- 【修改】`文本处理车间/结构化重塑/_skill_evolution/skill_loader.md`、`_prompts/write_loader.md`、`_prompts/README.md`、`README.md`：清理 examples 全部引用，技能文件收敛为三件套（spec/eval/loader），loader 步骤 5 改为以 eval 锚点做存疑裁决
- 【修改】`文本处理车间/结构化重塑/_skill_evolution/eval.md`：新增「适用性规则」（不适用项按满分计并备注「不适用」），消除清单偏对比类内容对矩阵/认知模式的不公平
- 【修改】`文本处理车间/结构化重塑/_skill_evolution/spec.md`：§1 明确 prompt 模式内的角色为本角色的子角色、叠加生效
- 【修改】`文本处理车间/结构化重塑/_skill_evolution/skill_loader.md`、`_prompts/write_loader.md`：重写红线加上限（最多 2 次，仍不达标则输出最优版并附差距说明）
- 【修改】`文本处理车间/结构化重塑/_skill_evolution/spec.md`、`eval.md`：标题补 v1.0，三件套版本号统一；`_prompts/write_loader.md` 版本号规则改为三件套共用、与 prompt 版本解耦
- 【新增】`_config/global_rules.md`：注意事项补充「prompt 升版改名时须同步更新对应 loader 引用路径」，闭环硬编码路径断链风险
- 【新增/试点】`文本处理车间/结构化重塑/skill_v1.0.md`：单文件技能样板（加载说明+Spec+Eval+提示词模板四章合一，自包含可粘贴），**待用户确认**；原 `prompt_v0.1.md` 与 `_skill_evolution/` 暂保留
- 【迁移】全仓切换至单文件技能体系：新增 `_prompts/write_skill.md` 统一编写器（删除 write_spec/write_eval/write_loader）；重写 `_prompts/README.md`、`_config/global_rules.md`（判定标准改为四章合一、自包含）、`README.md`；`文本处理车间/结构化重塑/` 的 `_skill_evolution/` 三件套与 `prompt_v0.1.md` 确认并入 `skill_v1.0.md` 后删除
- 【重构】验收机制去打分化：`文本处理车间/skill_v1.0.md`、`_prompts/write_skill.md`、`_config/global_rules.md`、`README.md`、`_prompts/README.md`——废除 1-5 分评分表/合格线，改为红线二元核验（R1 零编造一票否决）+ 对照原文双向追溯 + 强制风险披露，高风险场景可选批评者二审
