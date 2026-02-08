# WHMCS Lava.ru Payment Gateway

Модуль платежного шлюза для интеграции платежной системы **Lava.ru** (Business API) с биллинг-панелью **WHMCS**.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![AI: Claude](https://img.shields.io/badge/AI-Claude-blueviolet)

## 🤖 О проекте

Этот модуль позволяет принимать платежи от клиентов через сервис Lava.ru.
**Важно:** Код данного проекта был полностью написан с использованием нейросети **Claude** (Anthropic).

## ✨ Возможности

*   Создание счетов через API Lava.ru (Business).
*   Автоматическая генерация подписи (HMAC SHA256).
*   Настройка времени жизни счета.
*   Логирование запросов и ответов в "Module Log" WHMCS для отладки.
*   Поддержка перенаправления клиента после успешной оплаты.

## 🚀 Установка

1.  Скачайте файл модуля (например, `lava.php`).
2.  Загрузите файл в директорию вашего WHMCS:
    `/modules/gateways/lava.php`
3.  *(Опционально)* Убедитесь, что у вас есть файл обработки callback-ов по пути `/modules/gateways/callback/lava.php` (он необходим для автоматического зачисления платежей).

## ⚙️ Настройка

1.  Зайдите в админ-панель WHMCS.
2.  Перейдите в **Настройки** -> **Приложения и интеграции**.
3.  Найдите и активируйте **Lava**.
4.  Заполните поля конфигурации:
    *   **Shop ID**: UUID вашего проекта из личного кабинета Lava.ru.
    *   **Secret Key**: Секретный ключ для подписи запросов (из настроек проекта в Lava).
    *   **Webhook Key**: Дополнительный ключ для проверки уведомлений (если используется).
    *   **Expire (minutes)**: Время жизни ссылки на оплату (по умолчанию 60 минут).
5.  Сохраните изменения.

## 📝 Лицензия

Этот проект распространяется под лицензией **MIT**.

```text
MIT License

Copyright (c) 2026 TenHopesForOneSolution

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## ⚠️ Отказ от ответственности

Данный код предоставлен "как есть". Пожалуйста, протестируйте модуль в среде разработки (Dev mode) перед использованием на реальном проекте. Автор и разработчик ИИ не несут ответственности за возможные финансовые потери или ошибки в работе модуля.
