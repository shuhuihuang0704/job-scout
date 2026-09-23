# Job Scout · 公开岗位雷达

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> 面向 AI 助手的 Codex skill：搜索公开招聘信息，核验原帖，提炼岗位要求，并按你的条件比较机会。

Job Scout 适合查找全职、实习、合同等公开岗位。它尽量保留原始招聘链接和可核验的证据，帮助你快速判断哪些机会值得进一步了解。

## ✨ 能做什么

- **搜索岗位**：按岗位、城市、工作方式、薪资和经验查找公开机会。
- **核验来源**：优先查看雇主官网、招聘负责人原帖或可识别的原始页面。
- **提炼要求**：整理职责、技能、经验、学历、地点、工作形式和薪资。
- **比较机会**：区分硬性条件与偏好，说明匹配点、缺口和未知信息。
- **保留证据**：附上原帖链接、发布日期、状态和来源限制。
- **控制预算**：记录每次搜索动作、成本和剩余预算。

## 🚀 安装

将完整仓库安装到 Codex skills 目录：

```bash
git clone https://github.com/shuhuihuang0704/job-scout.git "$CODEX_HOME/skills/job-scout"
```

没有设置 `CODEX_HOME` 时使用：

```bash
git clone https://github.com/shuhuihuang0704/job-scout.git "$HOME/.codex/skills/job-scout"
```

更新已有安装：

```bash
git -C "$CODEX_HOME/skills/job-scout" pull --ff-only
```

安装后确认目录中存在 `SKILL.md`、`agents/`、`references/` 和 `LICENSE`，然后重新加载 skill 或重启 Codex。

## 🧭 工作方式

1. 提取岗位、城市、工作类型、经验、薪资、办公方式和预算等条件。
2. 用少量关键词变体搜索公开来源，不悄悄放宽硬性条件。
3. 回到雇主页面或明确的招聘原帖，核验岗位状态、要求和日期。
4. 去重后按硬性条件、来源可靠性、新鲜度和偏好整理短名单。

如果你只提供招聘链接，Job Scout 可以直接分析链接；没有搜索或浏览能力时，它不会假装自己找到了新岗位。

## 💬 使用示例

```text
使用 $job-scout 找宁波的 AI 产品岗位，实习也可以。最多花 5 积分，给我招聘原帖和岗位要求，我先挑几家。
```

## 📋 输出内容

每条结果尽量包括：岗位与公司、地点与办公形式、工作类型、发布时间、岗位要求、原始链接、匹配说明，以及无法确认的部分。

## 🛡️ 边界与隐私

- 只使用公开网页，不绕过登录、权限、付费墙或验证码。
- 不自动投递简历、不联系招聘方、不发送邮件、不上传个人资料。
- 不内置岗位数据库、私有 API、账号或凭证。
- 不把结果当成穷尽列表；无法打开或信息不完整时会明确标注。

## 📁 项目结构

```text
job-scout/
├── SKILL.md
├── CONTRIBUTING.md
├── LICENSE
├── agents/openai.yaml
└── references/
    ├── matching-rubric.md
    ├── search-strategy.md
    └── sources-and-evidence.md
```

## 🤝 维护与贡献

仓库采用 [MIT License](LICENSE)。提交修改前请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)，并运行：

```bash
git diff --check
```

更多规则见 [`SKILL.md`](SKILL.md) 和 [`references/`](references/)。

## English summary

Job Scout is a Codex skill for finding and comparing public job postings. It verifies original listings when possible, summarizes requirements, preserves source links, and labels uncertainty. It does not apply for jobs, contact recruiters, upload resumes, or use private credentials.
