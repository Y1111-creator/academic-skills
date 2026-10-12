# 学术写作 Skills

用于论文结构重整、文字精简、学术写作、审稿检查和本地文献整理。

| Skill | 用途 |
| --- | --- |
| academic-writing | 中文和英文论文的结构、论证与段落递进 |
| manuscript-writing-review | 删除冗余表达、改善句子结构、统一术语 |
| paper-polishing-v1 | 期刊论文结构诊断与润色 |
| scientific-writing | 科学写作及内容一致性检查 |
| peer-review | 审稿视角的证据、方法与统计检查 |
| citation-management-offline | 本地参考文献整理与 BibTeX 去重 |

文件位于 [`.agents/skills/`](.agents/skills/)，每个 skill 的入口是 `SKILL.md`，配套资料在同一目录。

建议先调整论文主线和章节功能，再精简语言，最后检查引用与全文一致性。原始数据、公式、图表和科学含义应保留。

在支持 Agent Skills 的环境中，可以按名称调用，例如 `$academic-writing`。保存在 GitHub 不会自动安装到所有应用，具体加载方式取决于使用的客户端。

各 skill 的来源、固定版本及导入变更记录在 `references/upstream-source.json`。已有上游许可证一并保留；没有声明许可证的项目没有因此获得新的转载许可。

文献管理保留的是离线精简版本，不包含联网检索或凭据读取脚本。本地格式检查不能证明文献真实性或文献对论述的支持程度。
