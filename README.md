# McpAutomationBridge for UE 5.7

Адаптированный плагин McpAutomationBridge для Unreal Engine 5.7.3

Оригинал: https://github.com/ChiR24/Unreal_mcp

## Изменения

В `McpAutomationBridge.uplugin` добавлено поле:
```json
"EngineVersion": "5.7.0"
```

Это позволяет плагину корректно определяться как совместимый с UE 5.7.x.

## Установка

1. Скопируйте папку `plugins/McpAutomationBridge` в папку `Plugins` вашего проекта
2. Откройте проект в Unreal Engine 5.7.3
3. При запросе на пересборку нажмите "Yes"

## Структура

```
YourProject/
└── Plugins/
    └── McpAutomationBridge/
        ├── McpAutomationBridge.uplugin
        ├── Config/
        └── Source/
            └── McpAutomationBridge/
```

## Требования

- Unreal Engine 5.7.x
- Включенные плагины (автоматически подключаются):
  - EditorScriptingUtilities
  - LevelSequenceEditor
  - Niagara/NiagaraEditor
  - И другие (см. `.uplugin`)

## Проблемы с компиляцией

Если при пересборке возникают ошибки:
1. Удалите папки `Binaries` и `Intermediate` внутри `McpAutomationBridge`
2. Попробуйте пересобрать через IDE (Visual Studio/Rider) вместо пересборки из редактора
3. Убедитесь, что все зависимые плагины включены в вашем проекте
