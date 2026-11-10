# Структура репозитория

```text
Windows-Agent-Hub/
├── .github/
│   └── copilot-instructions.md
├── config/
│   └── examples/
│       ├── clients.example.yaml
│       └── upstreams.example.yaml
├── docs/
│   ├── architecture/
│   │   ├── OVERVIEW.md
│   │   └── REPOSITORY_LAYOUT.md
│   ├── decisions/
│   │   └── 0001-hub-is-bridge.md
│   ├── integrations/
│   │   └── INTEGRATION_PLAN.md
│   ├── inventory/
│   │   └── HOME-PC.md
│   ├── providers/
│   │   ├── PROFILES.md
│   │   └── WEB_UI.md
│   └── STATUS.md
├── src/
│   └── hub/
│       ├── adapters/
│       ├── mcp/
│       ├── registry/
│       └── transport/
├── tasks/
│   ├── chatgpt/
│   ├── claude/
│   ├── copilot/
│   ├── cursor/
│   ├── desktop-commander/
│   ├── gemini/
│   ├── manual/
│   ├── qwen/
│   ├── uivision/
│   └── vscode-copilot/
├── tests/
│   └── contracts/
├── .gitignore
├── LICENSE
├── PLAN.md
└── README.md
```

Пустые каталоги сохраняются README/TODO-файлами до появления реализации. Новые каталоги добавляются только под подтверждённые интеграции. Структура намеренно минимальна: никакого Planner, Router, Supervisor, Verifier или agent runtime.
