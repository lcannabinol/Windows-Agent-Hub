# Архитектура: HUB как MCP bridge

## Граница ответственности
Вне HUB (AI-клиент): понимание естественного языка, выбор модели, планирование, выбор инструмента, анализ результата, повторы и перепланирование.

Внутри HUB: MCP server/gateway, реестр upstream MCP, транспортная маршрутизация, фильтрация инструментов по профилю клиента, возврат результатов и ошибок, диагностика соединений.

HUB не интерпретирует stdout/stderr и не утверждает, что пользовательская задача выполнена успешно.

## Поток
AI client → MCP connection → HUB → upstream MCP/adapter → Windows tool.
Ответ возвращается по обратному маршруту без смысловой переработки.

## Категории
AI clients/agents: Claude Desktop, Cursor, Qwen Code, VS Code/Copilot, ChatGPT и другие MCP-клиенты.

AI web interfaces: ChatGPT Web, Gemini Web, Qwen Web. Browser automation — отдельный канал, не эквивалент API/MCP.

Upstream tools: Remote Desktop Commander/Desktop Commander, Google Data Cloud MCP, Ui.Vision, Playwright/CDP, AutoHotkey, локальные OCR/STT/TTS-компоненты.

## Профили
Профиль клиента описывает client_id, тип клиента, транспорт, возможности, доступные группы инструментов, ограничения и ссылку на локальную авторизацию. Секреты и cookies в профиле не хранятся.

Отдельный Python runtime для каждого AI-сервиса не создавать. Изоляция — только при доказанном конфликте зависимостей.

## Модули
- mcp/: входящий MCP server и типы протокола.
- registry/: upstream-серверы и инструменты.
- adapters/: интеграции конкретных систем.
- transport/: stdio/HTTP и соединения.
- config/: клиентские профили и upstream.
- logging/: технические события и диагностика.

Не создавать Planner, Supervisor, AI Router, Task Engine, Verifier, Intent Engine или обязательную локальную LLM.

## Ограничения
- По умолчанию localhost.
- Не публиковать все инструменты всем клиентам.
- Admin/destructive tools выключены в стандартном профиле.
- Нет произвольного shell и автоматического UAC elevation.
- Секреты и browser sessions остаются в локальном защищённом хранилище.
- Малое потребление CPU/RAM; Windows 10 x64; Python 3.11.
- Новые компоненты на D:; не требовать GPU и платных API.
