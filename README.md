# alanthssss

Share Site

## Copilot portfolio refresh

The manually triggered `Refresh portfolio with Copilot` workflow reads the
owner's current pinned repositories and asks GitHub Copilot coding agent to
redesign or refresh the site in a pull request.

### One-time setup

1. Enable GitHub Actions and GitHub Copilot coding agent for this repository.
2. Create a fine-grained personal access token for this repository with read
   access to metadata and read/write access to Actions, Contents, Issues, and
   Pull requests. A classic token can instead use the `repo` scope.
3. Add the token as a repository Actions secret named `COPILOT_PAT`.

The token must belong to a user with a paid Copilot plan and access to Copilot
coding agent in this repository.

### Run a refresh

Open **Actions → Refresh portfolio with Copilot → Run workflow**. Extra design
direction and a supported model ID are optional. When no model is supplied,
Copilot selects one automatically.

The workflow fetches up to six pinned repositories from `alanthssss`, starts a
Copilot agent task, and requests a pull request. Review and merge that pull
request to publish the update through the existing GitHub Pages workflow.

GitHub's agent tasks API is currently in public preview.
