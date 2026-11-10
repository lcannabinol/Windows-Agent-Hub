# Copilot instructions

This repository is a local MCP bridge for Windows, NOT an autonomous AI agent.

Never add Planner, Supervisor, AI Router, Verifier, autonomous task orchestration, or mandatory local LLM.

Core behavior:
- Accept MCP client connections.
- Publish a filtered catalog of upstream tools.
- Forward tool calls to selected upstream MCP servers/adapters.
- Return upstream results/errors without interpreting task success.
- Expose technical connection status only.

Constraints:
- Python 3.11, Windows 10 x64.
- New files, environments, caches and models belong on D:.
- Do not install/move software on C:.
- Reuse existing Desktop Commander, Google MCP proxy, Ui.Vision, AutoHotkey and VoiceAssistant where applicable.
- Never commit API keys, OAuth tokens, cookies or browser sessions.
- Do not alter existing user MCP configs without explicit approval.
- Keep dependencies minimal and test with mock MCP servers.
- Prefer free/open-source and already-installed components.
- No large code generation before presenting a concise implementation plan and confirming protocol choices.
