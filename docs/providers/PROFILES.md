# AI-клиенты и профили подключений

Профили описывают возможности конкретной версии клиента и канала. Отдельный Python venv не требуется.

| Клиент | Предпочтительный путь | Текущее состояние / проверка |
|---|---|---|
| Claude Desktop | MCP stdio | Desktop Commander уже прописан |
| Cursor | MCP stdio | mcp.json найден, mcpServers пуст |
| VS Code/Copilot | MCP stdio | 10 Google MCP через proxy |
| Qwen Code | MCP, если поддерживается версией | Проверить; Desktop Commander не считать доступным автоматически |
| ChatGPT | поддерживаемый remote MCP или текущий Remote Desktop Commander | проверить ограничения плана |
| Gemini Web | Browser UI | проверить DOM/CDP и сессию |
| Qwen Web | Browser UI | проверить DOM/CDP и сессию |
| ChatGPT Web | Browser UI | проверить DOM/CDP и сессию |
| Ollama | локальный API, необязательно | не делать обязательным |

Поля: id, client_type, connection_type, transport, capabilities, exposed_tool_groups, known_limitations, auth_reference, status_check.

Web UI не равен API. Tool calling проверяется для конкретной модели/версии/канала. Секреты, токены, cookies и browser sessions в Git не попадают. Платные API не являются обязательным путём.
