# 🎵 Music Catalog

Каталог музыкальных исполнителей, альбомов и треков.  
Fullstack-приложение на Next.js с загрузкой файлов, поиском и пагинацией.

🔗 **Демо (только чтение):** [music-catalog-sepia.vercel.app](https://music-catalog-sepia.vercel.app/)

> ⚠️ **Важно:** Демо-версия развёрнута на Vercel (read-only файловая система).  
> **Функции записи (создание/редактирование/удаление) и загрузка файлов в демо недоступны.**  
> Полный функционал работает при **локальном запуске** — см. инструкцию ниже.  
> Код проекта открыт, все API и компоненты можно посмотреть на [GitHub](https://github.com/smehovartem566/music-catalog).

---
## 🛠 Технологии

- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- React (хуки: useState, useEffect, useCallback)
- File API (загрузка обложек и аудио)
- JSON storage + fs (сохранение данных)

## 🚀 Запуск

```bash
git clone https://github.com/smehovartem566/music-catalog.git
cd music-catalog
npm install
npm run dev
```

Открой http://localhost:3000

## 📁 Сущности и связи

- **Исполнитель** → **Альбом** → **Трек** (один-ко-многим)
- Каждая сущность — полноценный CRUD

## 🔧 API

| Сущность | Эндпоинты |
|----------|-----------|
| Исполнители | GET /api/artists, POST /api/artists, GET/PATCH/DELETE /api/artists/:id |
| Альбомы | GET /api/albums (поиск, фильтр, пагинация), POST /api/albums, GET/PATCH/DELETE /api/albums/:id |
| Треки | GET /api/tracks?albumId=, POST /api/tracks, DELETE /api/tracks/:id |
| Файлы | POST /api/upload (cover / audio) |

## ✨ Реализовано

- Загрузка обложек и аудио (Drag & Drop)
- Поиск по альбомам с debounce
- Пагинация
- Адаптивный интерфейс
- Данные сохраняются в JSON-файл (не теряются после перезапуска)

## 👤 Автор

Артём Смехов — [GitHub](https://github.com/smehovartem566)
