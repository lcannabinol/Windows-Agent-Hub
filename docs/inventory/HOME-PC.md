# HOME-PC inventory — 2026-11-10

## Система
Windows 10 Pro build 19045 x64; Intel i7-6700 4C/8T; 16 GB RAM; AMD RX 580 4 GB; Python 3.11.9; Node.js 24.22.1; Git 2.56.0.4; VS Build Tools 2022; Java 21.

## AI и разработка
Cursor 3.29.15; Qwen Desktop 1.0.3; Qwen Code Desktop 0.0.5; Qwen Code CLI 0.26.1; VS Code 1.143.1; GitHub Desktop 3.6.10; GitHub Copilot 1.1.32.

## Автоматизация
Ui.Vision Desktop Automation 2.1.43; AutoHotkey 2.0.19; Edge 157; Chrome Remote Desktop extension; Copyfish OCR; ChatGPT; Blackbox; Read Aloud.

## MCP по предыдущему аудиту
- Claude Desktop: Desktop Commander через npx.
- VS Code: 10 Google Data Cloud MCP через общий proxy; 9 endpoint отвечают на handshake/tools/list, 114 tool definitions; Firestore 401.
- Cursor: mcp.json найден, mcpServers пуст.
- Remote Desktop Commander подключён.
- Qwen: конфигурация и поддержка MCP требуют проверки по установленной версии.

## Голос
D:\LLM\VoiceAssistant; Faster-Whisper small RU CPU INT8; Windows OCR API ru-RU; SAPI5 Microsoft Irina; hotkeys Ctrl+Alt+Space и Ctrl+Alt+Esc.

## Не подтверждено
Playwright; Ui.Vision browser extension в активном Edge профиле; актуальная работоспособность всех venv; MCP compatibility каждой версии клиента.

## Ограничения
Не устанавливать на C: без необходимости. Новые проекты, SDK, venv, caches и модели — на D:. Не переносить существующие приложения. Не читать/копировать токены, cookies и ключи.
