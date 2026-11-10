# GitHub Copilot — стартовое задание

Прочитать README.md, PLAN.md, docs/architecture/OVERVIEW.md и ADR-0001.

Реализовать минимальный MCP bridge:
1. Подключение к одному upstream MCP.
2. Получение tools/list.
3. Публикация списка клиенту.
4. Прозрачное перенаправление tools/call.
5. Возврат upstream result/error.

Запреты:
- Не добавлять Planner, Supervisor, AI Router, Verifier, agent loop или LLM.
- Не выполнять произвольный shell и не повышать UAC.
- Не добавлять обязательные платные API.
- Не менять MCP-конфиги пользователя.
- Не устанавливать ничего на C:.
- Не читать и не включать секреты.
- Не переписывать Desktop Commander/Ui.Vision.

Требования: Python 3.11, минимальные зависимости, mock MCP tests, таймауты и корректное закрытие соединений, логи без секретов.

Сначала выдать короткий implementation plan, выбрать MCP SDK/transport и список файлов. Не писать большой объём кода до согласования.
