# 🚛 РейсКонтроль

### Android + Web платформа для управления грузовыми рейсами, водителями, транспортом, расчётами и документами

![Status](https://img.shields.io/badge/Status-Active%20Development-success)
![Android](https://img.shields.io/badge/Android-Java-green?logo=android)
![Backend](https://img.shields.io/badge/Backend-Spring%20Boot-brightgreen?logo=springboot)
![Web](https://img.shields.io/badge/Web-Next.js-black?logo=next.js)
![Database](https://img.shields.io/badge/Database-PostgreSQL-blue?logo=postgresql)
![Docker](https://img.shields.io/badge/Infra-Docker-blue?logo=docker)

---

## 🎯 Что такое РейсКонтроль

РейсКонтроль — система для цифрового сопровождения грузовых перевозок.

Проект объединяет мобильное Android-приложение и web-платформу для работы с рейсами, водителями, транспортом, документами, расчётами и операционными данными.

> Этот репозиторий является публичной витриной проекта.  
> Основной исходный код, production-конфигурация, credentials и реальные пользовательские данные не публикуются.

---

## 🧩 Основные возможности

- создание и сопровождение грузовых рейсов;
- работа с водителями, автомобилями и прицепами;
- расчёт расходов и итогов рейса;
- учёт простоев, суточных и дополнительных операций;
- разные роли пользователей и ограничения доступа;
- OCR-разбор заявок и документов;
- экспорт данных и документов;
- web-кабинет логиста;
- REST API;
- PostgreSQL;
- Docker Compose;
- геокодирование и расчёт расстояний;
- security-first архитектура.

---

## 👥 Роли

### Логист
Работает с рейсами, клиентами, транспортом, водителями и операционными данными.

### Водитель своего грузовика
Видит данные своего рейса и собственные финансовые показатели.

### Наёмный водитель
Работает с назначенными рейсами, но не должен видеть прибыль логиста.

---

## 🏗 Архитектура

```text
                    ┌─────────────────────┐
                    │     РейсКонтроль    │
                    └──────────┬──────────┘
                               │
            ┌──────────────────┴──────────────────┐
            │                                     │
            ▼                                     ▼
     Android Application                    Web Platform
        Java / Room                        Next.js / Tailwind
            │                                     │
            └──────────────────┬──────────────────┘
                               ▼
                         REST API /api/v1
                               │
                         Spring Boot
                               │
                ┌──────────────┼──────────────┐
                ▼              ▼              ▼
           PostgreSQL       Documents      Geo Services
              RLS            Storage      Nominatim / OSRM
```

---

## 🛠 Технологии

**Mobile**

`Java` `Android` `Room` `JUnit` `Tesseract OCR`

**Backend**

`Spring Boot` `REST API` `PostgreSQL` `Docker`

**Web**

`Next.js` `TypeScript` `Tailwind CSS`

**Infrastructure & Security**

`Docker Compose` `PostgreSQL RLS` `Reverse Proxy` `Audit Logging`

**Geo**

`Nominatim` `OSRM`

---

## 🧪 Testing & Quality

В проекте используются:

- JVM unit tests;
- Android connected tests;
- Room migration tests;
- lint;
- build verification;
- security checks;
- `.env` / secret checks;
- regression testing;
- ручная проверка Android и web-сценариев.

Один из зафиксированных baseline-checkpoint проекта включал **116/116 JVM tests**, **15/15 Android connected tests**, `Lint PASS` и `.env security PASS`.

---

## 🔐 Security

Архитектура строится по принципу **защиты в глубину**:

- авторизация и проверка ролей на backend;
- Row-Level Security в PostgreSQL;
- закрытое файловое хранилище;
- reverse proxy;
- audit trail;
- минимизация разрешений Android;
- защита чувствительных данных;
- отдельные security-проверки перед релизом.

---

## 📚 Документация

- [Architecture](docs/architecture.md)
- [Mobile App](docs/mobile-app.md)
- [Web Platform](docs/web-platform.md)
- [Features](docs/features.md)
- [Roles & Permissions](docs/roles-and-permissions.md)
- [Testing](docs/testing.md)
- [Security](docs/security.md)
- [OCR & Documents](docs/ocr-and-documents.md)
- [Calculations](docs/calculations.md)
- [Tech Stack](docs/tech-stack.md)
- [Roadmap](docs/roadmap.md)
- [For Recruiters](docs/for-recruiters.md)
- [Showcase Scope](docs/showcase-scope.md)

---

## 📌 Статус

**Active development**

Проект развивается как полноценная Android + Web система для реальных сценариев грузоперевозок.

---

## 👤 Автор

**Илья Артамонов**

Junior QA Engineer • Technical Support • AI Automation

📍 Astana, Kazakhstan  
📧 korresdit@gmail.com  
💬 Telegram: [@Its_ilyawork](https://t.me/Its_ilyawork)
