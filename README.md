# alanthssss

Share Site / 分享站点

## Portfolio site structure / 作品集站点结构

The GitHub Pages portfolio is served directly from repository root static files:

- `/index.html` — semantic, responsive portfolio page
- `/assets/css/home.css` — page styling, color-scheme support, focus states, and reduced-motion behavior
- `/python/` and `/docker/` — preserved note collections linked from the portfolio

No build step, runtime JavaScript, or external runtime dependency is required for the root portfolio page.

GitHub Pages 作品集直接使用仓库根目录中的静态文件发布：

- `/index.html` — 语义清晰、支持响应式布局的作品集页面
- `/assets/css/home.css` — 页面样式、配色方案、焦点状态及减少动态效果支持
- `/python/` 和 `/docker/` — 从作品集链接进入的既有技术笔记

根目录作品集页面不需要构建步骤、运行时 JavaScript 或外部运行依赖。

## Copilot portfolio refresh / Copilot 作品集更新

The manually triggered `Refresh portfolio with Copilot` workflow reads the
owner's current pinned repositories and asks GitHub Copilot coding agent to
redesign or refresh the site in a pull request.

手动触发的 `Refresh portfolio with Copilot` workflow 会读取站点所有者当前置顶的
GitHub 仓库，并让 GitHub Copilot coding agent 通过 pull request 重新设计或更新网站。

### One-time setup / 初次配置

1. Enable GitHub Actions and GitHub Copilot coding agent for this repository.
2. Create a fine-grained personal access token for this repository with read
   access to metadata and read/write access to Actions, Contents, Issues, and
   Pull requests. A classic token can instead use the `repo` scope.
3. Add the token as a repository Actions secret named `COPILOT_PAT`.

1. 为本仓库启用 GitHub Actions 和 GitHub Copilot coding agent。
2. 创建仅用于本仓库的 fine-grained personal access token，授予 Metadata 读取权限，
   以及 Actions、Contents、Issues 和 Pull requests 读写权限；也可以使用具有 `repo`
   scope 的 classic token。
3. 将 token 添加为名为 `COPILOT_PAT` 的仓库 Actions Secret。

The token must belong to a user with a paid Copilot plan and access to Copilot
coding agent in this repository.

该 token 必须属于拥有付费 Copilot 方案、且能够在本仓库使用 Copilot coding
agent 的用户。

### Run a refresh / 运行更新

Open **Actions → Refresh portfolio with Copilot → Run workflow**. Extra design
direction and a supported model ID are optional. When no model is supplied,
Copilot selects one automatically.

The workflow fetches up to six pinned repositories from `alanthssss`, starts a
Copilot agent task, and requests a pull request. Review and merge that pull
request to publish the update through the existing GitHub Pages workflow.
Repository metadata is compacted and README excerpts are bounded so the task
stays within the Copilot agent API prompt limit.

打开 **Actions → Refresh portfolio with Copilot → Run workflow**。可以选择填写额外的
设计要求和受支持的模型 ID；留空时由 Copilot 自动选择模型。Workflow 会读取
`alanthssss` 最多六个置顶仓库的元数据及 README 摘要，启动 Copilot agent task，
并要求它创建 pull request。审核并合并该 PR 后，现有 GitHub Pages workflow 会发布更新。
仓库元数据会进行压缩，README 摘要也会限制长度，确保任务不超过 Copilot agent API 的
提示长度上限。

生成的作品集必须提供含义一致的简体中文和英文版本，并将每个置顶项目呈现为基于可验证
资料的简历式项目经历，而不是简单的 GitHub 数据快照。

GitHub's agent tasks API is currently in public preview.

GitHub agent tasks API 目前仍处于公开预览阶段。
