
<%*
const folder = tp.file.folder(true);

if (!["Лекции/HTML", "Лекции/CSS"].includes(folder)) {
  new Notice("Избери папка Лекции/HTML или Лекции/CSS в QuickAdd.");
  return;
}

const title = await tp.system.prompt("Заглавие на урока");

if (!title || !title.trim()) {
  new Notice("Не е въведено заглавие.");
  return;
}

const files = app.vault.getMarkdownFiles().filter(
  f => f.parent?.path === folder && f.path !== tp.file.path(true)
);

let maxNumber = 0;

for (const file of files) {
  const match = file.basename.match(/^(\d+)\s+-\s+/);
  if (match) maxNumber = Math.max(maxNumber, Number(match[1]));
}

const number = String(maxNumber + 1).padStart(2, "0");
await tp.file.rename(`${number} - ${title.trim()}`);
%>

# 📘 <% tp.file.title.replace(/^\d+\s+-\s+/, "") %>

> [!abstract] Какво ще науча?
> - Ще разбера основните понятия.
> - Ще мога да ги използвам на практика.

---

## 01 · Теория

Обяснение на темата със собствени думи.

### Основни понятия

- **Понятие 1** — обяснение.
- **Понятие 2** — обяснение.

---

## 02 · Примери с код

### HTML

```html
<div class="card">
  <h2>Здравей, свят!</h2>
  <p>Моят първи пример.</p>
</div>
```

### CSS

```css
.card {
  padding: 20px;
  border-radius: 12px;
  background-color: #f3f6fa;
}

.card h2 {
  color: #2563eb;
}
```

---

## 03 · Практически упражнения

- [ ] Задача 1 — приложи наученото.
- [ ] Задача 2 — промени примера.
- [ ] Задача 3 — направи собствен вариант.

---

## 04 · Често срещани грешки

> [!warning] Внимавай!
> Запиши тук грешките, които си допуснал, и как си ги поправил.

---

## 05 · Обобщение

- **Научих:** …
- **Трябва да упражня:** …
- **Следваща тема:** …
