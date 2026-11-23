

<%*
const folder = "CSS";
const files = app.vault.getMarkdownFiles()
  .filter(f => f.parent?.path === folder);

const numbers = files.map(f => {
  const match = f.basename.match(/^(\d+)\s+-/);
  return match ? Number(match[1]) : 0;
});

const next = Math.max(0, ...numbers) + 1;
const number = String(next).padStart(2, "0");
const topic = await tp.system.prompt("Тема на CSS урока");

await tp.file.rename(`${number} - ${topic || "Нов урок"}`);
%>
---
type: css
date: <% tp.date.now("YYYY-MM-DD") %>
status: learning
tags:
  - css
---

# <% tp.file.title %>

## 🎯 Какво представлява?

## 💻 CSS синтаксис

```css

```

## 📝 Примери

### Пример 1

```css

```

**Обяснение:**

## 🎨 Свойства и стойности

| Свойство | Стойност | Описание |
|---|---|---|
| | | |

## 📌 Важни неща за запомняне

- 

## 🏋️ Практически упражнения

- [ ] Упражнение 1
- [ ] Упражнение 2
- [ ] Упражнение 3

## ⚠️ Често срещани грешки

- 

## 💡 Какво научих?

## ❓ Въпроси за преговор

## 🔗 Свързани уроци

## 📚 Източници
