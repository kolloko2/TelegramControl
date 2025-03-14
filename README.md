# 🚀 TeleChannel Manager - Windows Client 

**Управляйте Telegram-каналами как профессионал через безопасное Windows-приложение**  
![GitHub release](https://img.shields.io/badge/Platform-Windows-0078D6?logo=windows) 
![GitHub license](https://img.shields.io/badge/License-GPL--3.0-blue)

---

### 🌟 **Ключевые возможности**

| **Функция**               | **Описание**                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| 🔐 **Безопасное хранение** | Все ключи ботов шифруются AES-256 и хранятся только на вашем сервере        |
| 📢 **Умная публикация**    | Планирование постов, Rich-текст + медиавложения, шаблоны контента           |
| 🛡️ **Модерация**          | Автоудаление комментариев по фильтрам, бан-листы, антиспам                  |
| 📊 **Аналитика**           | Просмотр статистики в реальном времени, экспорт в Excel/PDF                 |
| 🤖 **Бот-менеджер**        | Централизованное управление подключениями ботов с правами доступа           |

---

### 🛠 **Архитектура**

```plantuml
@startuml

[Windows Client] -> [Server]: HTTPS/TLS 1.3\n(авторизация)
[Windows Client] <- [Server]: JWT-токен
[Server] -> [Telegram API]: MTProto\n(через ваши боты)
[Windows Client] -> [Server]: Все операции через gRPC

@enduml
