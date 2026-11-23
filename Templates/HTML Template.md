
<%*
const folder = "Лекции/HTML";
const files = app.vault.getMarkdownFiles()
  .filter(f => f.parent?.path === folder);

const numbers = files.map(f => {
  const match = f.basename.match(/^(\d+)\s+-/);
  return match ? Number(match[1]) : 0;
});

const next = Math.max(0, ...numbers) + 1;
const number = String(next).padStart(2, "0");

const topic = await tp.system.prompt("Тема на HTML урока");

await tp.file.rename(`${number} - ${topic || "Нов урок"}`);
%>
---
type: html
date: <% tp.date.now("YYYY-MM-DD") %>
status: learning
tags:
  - html
---

# <% tp.file.title %>

## 🎯 Какво представлява?

Обяснение на темата със собствени думи.

## 💻 Основен синтаксис

```html

```

## 📝 Примери

### HTML

```html

```

**Обяснение:**

## 📌 Важни неща за запомняне

- 

## 🏋️ Практически упражнения

- [ ] Упражнение 1
- [ ] Упражнение 2
- [ ] Упражнение 3

## ⚠️ Често срещани грешки

- 

## 💡 Какво научих?

Моето обобщение:

## ❓ Въпроси за преговор

- 

## 🖼️ Изображения

<!-- Добави изображенията от папка Изображения тук -->

## 🔗 Свързани уроци

## 📚 Източници




