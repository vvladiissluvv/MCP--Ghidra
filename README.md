# MCP--Ghidra
данный плагин разворачивает полноценный MCP-сервер внутри Ghidra, предоставляя AI-клиентам (например, Cursor или Claude Desktop) доступ к инструментам реверс-инжиниринга.

Шаг 1: Подготовка окружения (Prerequisites). Перед установкой убедитесь, что на вашем ПК установлены следующие компоненты:
Ghidra (рекомендуется стабильная версия, например, 11.x или 12.x).
Java JDK 21 и сборщик Maven (необходим для компиляции Java-части плагина).
Python 3.10+ (для запуска скриптов автоматизации установки и моста).
Инструмент uv (быстрый менеджер пакетов для Python, используется в примере конфигурации MCP).

Шаг 2: Клонирование репозитория и установка зависимостей
Откройте терминал (или PowerShell / командную строку на Windows) и выполните команды:
```bash
# Клонируем репозиторий проекта
git clone https://github.com/bethington/ghidra-mcp.git
cd ghidra-mcp
```
Далее скрипту автоматизации нужно импортировать JAR-файлы вашей установленной Ghidra в локальный репозиторий Maven. Замените /path/to/ghidra на реальный путь к папке, где распакована Ghidra (например, C:\ghidra_12.0.4_PUBLIC на Windows или /opt/ghidra на Linux):
```bash
# Импорт зависимостей Ghidra в Maven
python -m tools.setup install-ghidra-deps --ghidra-path "/path/to/ghidra"
```

<img width="833" height="320" alt="image" src="https://github.com/user-attachments/assets/c17973b1-d75d-40d1-b950-787a172e4176" />
