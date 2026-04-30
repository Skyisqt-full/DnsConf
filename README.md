# DNS Block&Redirect Configurer

Java-утилита для автоматизации DNS block/redirect правил в Cloudflare и NextDNS. Проект показывает работу с внешними API, конфигурацию через environment variables/secrets и запуск по расписанию через GitHub Actions.

## Бизнес-задача

Когда DNS-политики, blocklists и redirect rules нужно обновлять регулярно, ручная настройка быстро становится неудобной. Этот проект автоматизирует применение правил и подходит как основа для внутреннего infrastructure/admin tooling.

## Возможности

- Поддержка Cloudflare и NextDNS.
- Загрузка источников правил из внешних hosts/blocklist файлов.
- Разделение redirect и block сценариев.
- Обновление конфигураций через provider API.
- Запуск по cron через GitHub Actions.
- Конфигурация через secrets и environment variables.

## Стек

- Java.
- Maven/Gradle.
- GitHub Actions.
- Cloudflare API.
- NextDNS API.

## Основные переменные

- `DNS` - провайдер: `Cloudflare` или `NextDNS`.
- `AUTH_SECRET` - API token/key провайдера.
- `CLIENT_ID` - account/profile id.
- `REDIRECT` - источники redirect rules.
- `BLOCK` - источники block rules.

## Что является демонстрационным

Основной flow работает с реальными provider API, но реальные credentials должны передаваться только через GitHub Actions secrets или локальные environment variables. Репозиторий не содержит API tokens.

## English short version

Java automation utility for Cloudflare and NextDNS block/redirect rules with external API integration and GitHub Actions scheduling.
