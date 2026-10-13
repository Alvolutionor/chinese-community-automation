# Chinese Community Automation

**A Chinese-community extension of [reddit-automation](https://www.skills.sh/flowkit-labs/skills/reddit-automation), originally created by [doany.ai](https://doany.ai).**

Find genuine product-related requests in Chinese communities, check whether a
product can help, and draft useful replies with transparent affiliation disclosure.
This independently maintained extension adapts the original discovery-and-reply
workflow to Chinese platforms. It is not affiliated with the original authors or
any covered platform.

## Install

```bash
npx skills add Alvolutionor/chinese-community-automation --skill chinese-community-automation
```

For a global installation targeting specific agents:

```bash
npx skills add Alvolutionor/chinese-community-automation --skill chinese-community-automation -g -a codex -a claude-code
```

The skill uses the agent's existing search, browser, or connector capabilities.
It does not install a scraper, browser extension, MCP server, or publishing API.

## Use

Provide the product name or public URL, your actual relationship to the product,
and any known audience or platform preferences. For example:

```text
Use $chinese-community-automation to find genuine requests in Chinese communities
for my product. Product: [public URL]. I am its developer. Start with Xiaohongshu,
Zhihu, and V2EX, and return original discussion links, evidence of product fit,
and useful Chinese reply drafts.
```

You can also supply a specific discussion and request a reply. User-facing output
defaults to Simplified Chinese unless another language is requested. Platform
references are loaded only when needed.

## Platform coverage

Coverage means platform-specific research and writing guidance, not a live or
tested integration with every platform. Login requirements, inaccessible comments,
local rules, and available tools can limit a particular run.

| Platform or community | Supported surfaces |
| --- | --- |
| Xiaohongshu / XHS / rednote | Notes and specific comment requests |
| Zhihu | Questions, answers, and comments |
| V2EX | Topics and node-specific discussions |
| Juejin | Technical articles, comments, and short discussions |
| CSDN | Technical Q&A, blogs, and community discussions |
| SegmentFault | Technical Q&A and article discussions |
| Bilibili | Video, article, and dynamic-post discussions |
| Douban | Relevant groups and discussions subject to local rules |
| Baidu Tieba | Bar-specific help and designated discussion threads |
| Weibo | Explicit public requests and relevant replies |
| Douyin | Video context and specific comment requests |
| WeChat | Accessible public articles/Channels and supplied or narrowly authorized group context |
| OSCHINA | Open-source projects, technical Q&A, and discussions |
| SSPAI | Workflow and product-related discussions |
| 52pojie | Relevant software requests subject to current forum rules |
| LINUX DO | Demand research and rule review; no paste-ready AI outreach text |

LINUX DO has specific restrictions on AI-generated or polished text in its
[guidelines](https://linux.do/guidelines). Its adapter therefore provides research
and rule review. Other adapters also require checking the current rules for the
actual surface and account before product promotion.

## What a run returns

- A compact shortlist with original discussion links and the requester's actual need.
- A product-fit explanation and qualitative priority based on observable evidence.
- A platform-appropriate reply draft when sufficient evidence and rules support one.
- Separate pending leads when only snippets or incomplete context are available.
- The search scope and any meaningful access or verification limits.

The skill does not publish posts, send messages, buy engagement, generate fake
testimonials, or bypass platform access controls. It does not claim an unpublished
draft has been posted. A separate explicit publishing request requires suitable,
authorized tools and current platform rules.

## Differences from the original Reddit skill

- Routes across 16 Chinese platforms and communities instead of subreddits.
- Adapts Chinese search phrasing and reply depth to each content surface.
- Separates original-post requests from help requests inside comments.
- Tracks verified discussions separately from search snippets and inaccessible leads.
- Handles local group, bar, node, and board rules as well as platform rules.
- Addresses applicable commercial disclosure, off-platform diversion, and AI-content guidance.
- Uses first-person experience only when the user has actually supplied evidence.

## Provenance and license

The starting point is the [reddit-automation listing](https://www.skills.sh/flowkit-labs/skills/reddit-automation)
provided by the user, distributed in [flowkit-labs/skills](https://github.com/flowkit-labs/skills).
That repository credits [doany.ai](https://doany.ai) and links to the original
[doany-skills/skills](https://github.com/doany-skills/skills) project.

The referenced distribution was inspected at commit
[`0c9e2b63f504a296a86e45ed3a60a426dd979ca6`](https://github.com/flowkit-labs/skills/tree/0c9e2b63f504a296a86e45ed3a60a426dd979ca6).
The extension instructions are written for Chinese communities. They preserve the
original contribution-first approach while adding the platform adapters and
evidence workflow described above.

This project is distributed under the [MIT license](LICENSE). The original
`Copyright (c) 2026 doany.ai` notice is retained alongside the extension's copyright.
The installable skill folder contains its own copy of that license.

Platform references record their verification date and any inaccessible or
unverified policy material. They do not replace current official rules.
