<div align="center">

# 💬 GIN-Chat

### Автономная Защищенная Коммуникационная Платформа (E2EE WebRTC & Zero-Knowledge)

<br/>

[![Security: E2EE AES-256-GCM](https://img.shields.io/badge/Security-E2EE%20AES--256--GCM-00C853?style=for-the-badge&logo=shield)](https://github.com/GinCz/GIN-Chat)
[![Calls: WebRTC DTLS/SRTP](https://img.shields.io/badge/Calls-WebRTC%20DTLS%2FSRTP-2979FF?style=for-the-badge&logo=webrtc)](https://github.com/GinCz/GIN-Chat)
[![PWA: Cross-Platform](https://img.shields.io/badge/PWA-Windows%20%7C%20Android%20%7C%20iOS-AA00FF?style=for-the-badge&logo=pwa)](https://github.com/GinCz/GIN-Chat)
[![License: Proprietary Showcase](https://img.shields.io/badge/License-Proprietary%20Showcase-grey?style=for-the-badge)](https://github.com/GinCz/GIN-Chat)
[![Authors: Vladimir + AI](https://img.shields.io/badge/Authors-Vladimir%20%2B%20Anti--Gravity%20AI-FF6D00?style=for-the-badge)](https://github.com/GinCz/GIN-Chat)

<br/>

**GIN-Chat** — это автономная, приватная коммуникационная платформа с бескомпромиссным уровнем безопасности, сквозным шифрованием по модели *Zero-Knowledge*, защищенными WebRTC аудио/видеозвонками и чистым интерфейсом в стиле современных мессенджеров.

</div>

---

> [!IMPORTANT]
> **Политика конфиденциальности исходного кода (Proprietary Code Policy):**  
> Все полные исходные коды (серверный движок Node.js/SQLite, криптографические алгоритмы E2EE, PWA-клиент, медиа-компрессоры и нативные мобильные сборки) являются закрытой интеллектуальной собственностью и надежно хранятся в защищенном приватном хранилище автора ([Secret_Privat ↗](https://github.com/GinCz/Secret_Privat)).  
> Данный публичный репозиторий выступает исключительно в качестве **архитектурной витрины (Showcase)**, технической спецификации протоколов безопасности и эталона системной интеграции.

---

<br/>

## 🌟 Ключевые Преимущества и Архитектура Безопасности

<br/>

### 🛡️ 1. Сквозное E2EE-Шифрование (Zero-Knowledge Architecture)
* 🔐 **Криптография на клиенте:** Все текстовые сообщения и отправляемые файлы шифруются непосредственно на конечном устройстве пользователя (в браузере или приложении) с помощью стандарта **AES-256-GCM** через нативный **Web Crypto API**.
* 🚫 **Сервер ничего не знает:** Сервер выступает исключительно в роли «слепого почтальона» для зашифрованных бинарных пакетов. Даже при полном физическом доступе к серверу или дампу базы данных прочитать переписку математически невозможно — приватные ключи генерируются и хранятся только в памяти устройств собеседников.
* 🔒 **Защита персональных данных:** Номера телефонов, адреса электронной почты и системные идентификаторы скрыты от всех обычных участников диалогов.

<br/>

### 📞 2. Защищенные Голосовые и Видеозвонки (WebRTC)
* 🎙️ **Прямая P2P-связь:** Аудио- и видеоразговоры передаются напрямую между устройствами собеседников без промежуточного сохранения на сервере.
* 🛡️ **Криптографические протоколы DTLS 1.3 и SRTP:** Медиапотоки шифруются аппаратными алгоритмами защиты в режиме реального времени, исключая прослушивание, перехват или запись разговоров операторами связи.
* ⚡ **Высокое качество и адаптивный битрейт:** Автоматическая адаптация битрейта под текущую скорость интернет-соединения, кристально чистый звук и HD-видео.

<br/>

### 🌍 3. Автономный Выделенный Сервер без Блокировок
* 🚀 **Прямой выделенный канал:** Чат работает на автономном изолированном сервере с прямым DNS-маршрутом (без использования сторонних прокси-сетей и блокируемых CDN).
* 🌐 **100% Доступность 24/7:** Мгновенное открытие и стабильная работа из **любой точки мира** без необходимости использовать VPN.
* ⚡ **Высокая производительность:** Асинхронная архитектура на базе Node.js, SQLite с журналом опережающей записи (WAL) и Nginx с оптимизацией HTTP/2.

<br/>

---

<br/>

## 📱 Мультиплатформенный Доступ (PWA и Native Android)

* 🌐 **Мгновенный вход через любой браузер:** Google Chrome, Safari, Mozilla Firefox, Microsoft Edge, Yandex Browser.
* 📲 **Установка в 1 клик как PWA-приложение:** Поддержка нативного добавления на домашний экран Windows, Android, macOS и iOS с поддержкой офлайн-кэширования интерфейса и фоновых уведомлений.
* 🎬 **Связка с медиа-экосистемой:** Полная интеграция с нативными Android-приложениями линейки GinCz ([Android APK Suite ↗](https://github.com/GinCz/Android)).

<br/>

---

<br/>

## ⚙️ Сводная Спецификация Функций

| Модуль | Возможности и Технологический Стек |
| :--- | :--- |
| 💬 **Личные диалоги и комнаты** | E2EE переписка, автоудаление сообщений по таймеру (Burn on Read), статус доставки и прочтения. |
| 📞 **WebRTC Звонки** | Защищенный DTLS/SRTP peer-to-peer аудио/видео обмен, демонстрация экрана (Screen Sharing). |
| 📎 **Обмен медиафайлами** | Клиентское шифрование фото, видео, голосовых заметок и документов до 50 МБ. |
| 🎨 **Стикеры и реакции** | Нативные 3D-эмодзи, авторские наборы стикеров и реакции на сообщения. |
| 👥 **Групповые каналы** | Закрытые групповые чаты с разграничением прав участников и модерацией. |
| 👑 **Центр Управления** | Изолированная панель администратора: аудит сессий, одобрение пользователей, управление квотами. |

<br/>

---

<br/>

## 🌐 Архитектура Развертывания Nginx Reverse Proxy (Эталонный BluePrint)

Ниже представлена эталонная конфигурация защищенного периметра Nginx для обслуживания экземпляра GIN-Chat с поддержкой WebSocket (`WSS`) и HTTP/2:

```nginx
server {
    listen 80;
    server_name chat.example.com;
    return 301 https://$host$request_uri;
}

server {
    listen 443 ssl http2;
    server_name chat.example.com;

    ssl_certificate /etc/letsencrypt/live/chat.example.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/chat.example.com/privkey.pem;
    ssl_protocols TLSv1.2 TLSv1.3;
    ssl_ciphers HIGH:!aNULL:!MD5;

    client_max_body_size 50M;

    location / {
        proxy_pass http://127.0.0.1:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto https;
        proxy_read_timeout 86400s;
        proxy_send_timeout 86400s;
    }
}
```

<br/>

---

<br/>

<div align="center">

<h3>= Rooted by VladiMIR + AI =</h3>

<br/>

<a href="https://github.com/GinCz" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white" alt="GitHub" /></a>
&nbsp;&nbsp;<b>|||</b>&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/gincz/" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
&nbsp;&nbsp;<b>|||</b>&nbsp;&nbsp;
<a href="mailto:gin@volny.cz" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Email-gin%40volny.cz-blue?style=flat&logo=mail.ru&logoColor=white" alt="Email" /></a>

<br/><br/>

<sub>GIN-Chat &copy; 2026. Vladimir Bulantsev & Anti-Gravity AI · v.2026.10.22</sub>

</div>
