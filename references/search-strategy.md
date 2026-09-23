# Search strategy

Use this guide when the user's request needs query expansion, source ordering, or a freshness label. Keep the user's hard constraints unchanged while expanding wording.

## Query building

Build each query from:

role family + location + work type + one useful qualifier

Use a small set of close variants instead of a large synonym dump. For an AI product search, useful variants can include:

- AI 产品经理, AI 产品, 大模型产品, 生成式 AI 产品
- AI Product Manager, AI Product, GenAI Product
- AI 产品实习, 产品经理实习, Product Intern

Add the requested city in both Chinese and English when useful, such as 宁波 and Ningbo. Keep internship, full-time, contract, remote, and hybrid terms explicit when the user has stated them.

Do not replace a hard city or work-type constraint with a nearby city or a different employment type. If broadening could help, report the proposed broadening and ask first.

## Source order

1. Employer career page or employer-hosted requisition.
2. Identified recruiter or hiring-manager post that names the employer and role.
3. Public job board listing that appears to be the source.
4. Aggregator or search snippet, only as a lead to locate a stronger source.

Search snippets can discover a lead but cannot by themselves establish that a role is current or verified.

## Search rounds

Use the smallest number of rounds that can answer the request:

1. Exact role, city, and work type.
2. Close title variants and the same city.
3. Internship or entry-level variants only when the user allows them.

After each round, deduplicate roles and stop when the shortlist is sufficient or the user's budget is reached.

## Freshness

Use visible posting or update dates only for ranking:

- 最近发布: within roughly 7 days of the search date.
- 较早发布: older than 7 days, or the page shows an older update date.
- 日期未知: no visible date.

These labels do not change 招聘中, 已关闭, or 状态未知. Never estimate a date from search ranking, URL structure, or page appearance.

## Limited or blocked sources

Keep the direct URL when a page is blocked or incomplete. Mark the limitation beside the listing, use accessible corroborating sources when available, and do not present a snippet or copied summary as the original posting.
