# 🧪 Testing

В РейсКонтроле используются несколько уровней тестирования.

## Проверки

- JVM unit tests;
- Android connected tests;
- Room migration tests;
- lint;
- build verification;
- regression checks;
- security checks;
- ручные сценарии Android и web.

## Зафиксированный baseline

На одном из зафиксированных security-checkpoint:

- JVM: **116/116 PASS**
- Android connected: **15/15 PASS**
- Lint: **PASS**
- `.env` security: **PASS**

Текущий набор тестов продолжает меняться по мере развития проекта.
