# 🏗 Architecture

РейсКонтроль состоит из мобильного приложения и web-платформы с общим backend.

```text
Android App
    │
    ├── Local Room data
    │
    └─────────────┐
                  ▼
              REST API
                  │
             Spring Boot
                  │
        ┌─────────┼─────────┐
        ▼         ▼         ▼
   PostgreSQL  Documents   Geo
      RLS       Storage   Services
        ▲
        │
    Next.js Web
```

## Основные слои

- Android-клиент для работы в рейсе;
- web-кабинет для логиста;
- REST API `/api/v1`;
- PostgreSQL;
- файловое хранилище;
- геосервисы;
- security/audit слой.
