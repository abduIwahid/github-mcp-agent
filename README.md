# GitHub MCP Agent

Explore any GitHub repository in plain English. This agent connects to GitHub through the **Model Context Protocol (MCP)** — the same standard interface used by modern AI tooling — so it can inspect issues, pull requests and repository activity and answer questions about them conversationally.

## What it does

- Ask about open issues, active discussions, and PRs that need review
- Get repository health and activity summaries without clicking through GitHub
- Runs the official GitHub MCP server locally in Docker — your token never leaves your machine except to GitHub

## Tech stack

- **Streamlit** — web UI
- **Agno + MCP tools** — agent connected to the GitHub MCP server over stdio
- **Google Gemini 2.5 Flash** — reasoning model
- **Docker** — runs the official `ghcr.io/github/github-mcp-server`

## Run it locally

Prerequisites: Docker installed and running, a GitHub personal access token (repo scope), and a Google Gemini API key.

```bash
pip install -r requirements.txt
streamlit run github_agent.py
```

Paste both keys in the sidebar, name a repository in your question, and ask away.

## Example questions

- "What issues are being actively discussed in facebook/react?"
- "Show me recent merged PRs in this repository."
- "Which PRs are waiting for review?"

## Author

**Abdul Wahid** — AI/ML Developer
[Portfolio](https://www.abdulwahid.me) · [GitHub](https://github.com/abduIwahid) · [LinkedIn](https://www.linkedin.com/in/abdu1wahid)

## Credits

Adapted from a template in the [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) collection by Shubham Saboo, and reworked to run on Gemini instead of OpenAI. Licensed under Apache-2.0 — see [LICENSE](LICENSE).
