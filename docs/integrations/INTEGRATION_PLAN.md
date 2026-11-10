# Интеграция существующих компонентов

## Desktop Commander / Remote Desktop Commander
Используется для доступа к HOME-PC. Claude Desktop запускает @wonderwhy-er/desktop-commander через npx. Проверить возможность подключения существующего MCP как upstream. Не переписывать.

## Google Data Cloud MCP
VS Code config: C:\Users\Asus\AppData\Roaming\Code\User\mcp.json. 10 endpoint через общий mcp_proxy.js. 9 отвечают на initialize/tools/list, суммарно 114 описаний инструментов; Firestore HTTP 401. tools/list не подтверждает право выполнения. Подключать существующий proxy, не копировать auth.

## Ui.Vision
Desktop Automation 2.1.43 найден в C:\Users\Asus\AppData\Local\UI.Vision\DesktopAutomation; XModule native messaging manifests найдены. Extension в активном Edge профиле не подтверждён. Проверить фактический интерфейс, не предполагать MCP.

## Playwright/CDP
Наличие не подтверждено. Проверить установленный пакет, браузерные профили и CDP без повторной установки.

## AutoHotkey
2.0.19 установлен. Использовать именованные сценарии, не предоставлять произвольный запуск скриптов/shell.

## VoiceAssistant
D:\LLM\VoiceAssistant: Faster-Whisper small RU CPU INT8, Windows OCR API ru-RU, SAPI5 Microsoft Irina. STT — вход; OCR — отдельный инструмент; TTS — выход. Сохранить прототип, не переустанавливать.

## Ollama
Установлен; локальные Qwen GGUF обнаружены. Железо i7-6700, 16GB RAM, RX 580 4GB. Локальная LLM — необязательный эксперимент, не часть обязательного runtime.
