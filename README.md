# Job Scout · 公开岗位雷达

> 一个面向 AI 助手的 Codex skill：搜索公开招聘信息，核验原帖，提炼岗位要求，并按你的条件比较机会。

Job Scout 适合寻找全职、实习、合同等公开岗位。它会尽量保留原始招聘链接和可核验的证据，帮助你快速判断哪些机会值得进一步了解。

## ✨ 能做什么

- **搜索岗位**：根据岗位类型、城市、工作方式、薪资和经验要求查找公开机会。
- **核验来源**：优先查看雇主官网、招聘负责人原帖或可识别的原始招聘页面。
- **提炼要求**：整理职责、技能、经验、学历、地点、工作形式和薪资等信息。
- **比较机会**：区分硬性条件和偏好，说明匹配点、缺口与未知信息。
- **保留证据**：每条结果尽量附上原帖链接、发布日期和来源限制。
- **控制预算**：记录每次搜索动作、成本和剩余预算；无法确认成本时明确标注。
- **判断新鲜度**：根据页面显示的日期标记岗位新旧，但不把“较早发布”直接当成已关闭。

## 🚀 安装

### Codex

将完整的 job-scout 文件夹复制到：

~~~text
$CODEX_HOME/skills/job-scout
~~~

如果没有设置 CODEX_HOME，使用：

~~~text
~/.codex/skills/job-scout
~~~

然后重新加载 skill 列表，或重启 Codex。

### 从 GitHub 获取

~~~bash
git clone https://github.com/shuhuihuang0704/job-scout.git
~~~

复制完成后，确认目录中存在 SKILL.md、agents/ 和 references/。

## 💬 使用示例

~~~text
使用 $job-scout 找宁波的 AI 产品岗位，实习也可以。最多花 5 积分，给我招聘原帖和岗位要求，我先挑几家。
~~~

也可以指定更多条件：

~~~text
使用 $job-scout 找杭州的 AI 产品实习，优先互联网公司，接受远程，按原帖是否仍在招聘排序。
~~~

## 📋 输出内容

对于每个值得关注的岗位，Job Scout 会尽量提供：

| 字段 | 内容 |
| --- | --- |
| 岗位与公司 | 职位名称、雇主和团队信息 |
| 地点与形式 | 城市、办公方式和远程信息 |
| 工作类型 | 全职、实习、合同或原帖中的其他类型 |
| 发布时间 | 原帖展示的日期；没有时标记为“未显示” |
| 岗位要求 | 职责、技能、经验和学历要求的简要整理 |
| 原始链接 | 可直接打开的招聘原帖或雇主页面 |
| 匹配说明 | 与你给出的条件的匹配点、缺口和未知信息 |

如果用户设置了积分上限，还会显示预算账本：

~~~text
预算：5 积分
已使用：2 积分（或：成本未知）
剩余：3 积分（或：无法计算）
搜索动作：公开网页检索、原帖核验
~~~

## 🔎 搜索与核验流程

1. 提取你的岗位、城市、工作类型和明确限制。
2. 使用接近原意的职位关键词、城市别名和工作类型变体搜索公开来源。
3. 回到原始招聘页面核验岗位是否存在、是否仍然开放。
4. 按你的硬性条件和偏好整理短名单。
5. 输出预算账本、链接、要求、证据和无法确认的部分。

详细的关键词扩展、来源顺序和新鲜度规则见 references/search-strategy.md。

## 🛡️ 边界与隐私

- 只使用公开可访问的网页，不绕过登录、权限、付费墙或验证码。
- 不自动投递简历，不联系招聘方，不发送邮件，也不上传个人资料。
- 不内置岗位数据库、私有 API、账号或凭证。
- 不把搜索结果当成穷尽列表；来源覆盖和页面可访问性会影响结果。
- 如果原帖无法打开、已过期或信息不完整，会明确标注限制。

## 📁 项目结构

~~~text
job-scout/
├── SKILL.md                         # 核心 skill 指令
├── CONTRIBUTING.md                  # 修改和贡献说明
├── agents/openai.yaml               # Codex 展示信息与默认提示词
└── references/
    ├── matching-rubric.md           # 岗位匹配规则
    ├── search-strategy.md           # 搜索关键词、来源和新鲜度策略
    └── sources-and-evidence.md      # 来源与证据规则
~~~

## ⚙️ 使用要求

- 支持 SKILL.md 的 AI 助手。
- 可访问公开网页的搜索或浏览工具。

没有搜索或浏览能力时，仍可以让 Job Scout 分析你提供的招聘链接，但它无法自行发现新岗位。

## 🌱 发布前检查

如果要让其他人直接安装，请先将仓库设为公开，并选择合适的开源许可证。发布前还应确认安装路径、目标 AI 助手版本和公开网页访问能力与使用环境一致。

## English summary

Job Scout is a Codex skill for finding and comparing public job postings. It searches relevant sources, verifies original listings when possible, summarizes requirements, preserves source links, and clearly labels uncertainty. It does not apply for jobs, contact recruiters, upload resumes, or use private credentials.
