
<div align="center">
<h1>Деплой сервиса 'Место' на сервер с помощью pm2</h1>
<a href="https://github.com/VladislavSerKir/web-plus-pm2-deploy">
</a>
</div>

Развертывание сервиса 'Место' на облачном сервере

## Описание

* В качестве основной ОС для развертывания выбрана Linux ubuntu 20.04
* Для скачивания **npm пакетов** и работы **backend части** сервиса установлен пакет **node**
* Установлена **MongoDB** для работы сервиса с базой данных, а так же **Git** для скачивания кода непосредственно с репозитория сразу на сервер
* Установлена и настроена утилита **pm2** для непрерывной работы приложения. В случае ошибки приложение перезапустится автоматически. Точка входа приложения: `./dist/app.js`
* Для **маппинга** портов frontend и backend частей приложения, установлен и настроен **HTTP сервер nginx**. Для корректного отображения статики фронтенда прописаны правила обработки файлов и роутов:
  ![2023-07-20_20-53-33](https://github.com/VladislavSerKir/web-plus-pm2-deploy/assets/83783362/20c692d8-066d-4188-acd1-b3437c4ed2d7)
* Настроен backend на поддомене /api
* Выпущен сертификат **SSL** и настроено шифрование с помощью протокола **HTTPS**

## Развертывание
IP address `8130.193.37.247`

**Frontend** [https://vladislav.nomoreparties.sbs/](https://vladislav.nomoreparties.sbs/)

**Backend** [https://api.vladislav.nomoreparties.sbs/](https://api.vladislav.nomoreparties.sbs/)
## Написать мне
[![github](https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github)](https://github.com/VladislavSerKir)
[![telegram](https://img.shields.io/badge/Telegram-68c4f0?style=for-the-badge&logo=telegram)](https://t.me/vl_kireev)
