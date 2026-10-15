<%*
const folder = "Лекции/HTML";
const files = app.vault.getMarkdownFiles()
  .filter(f => f.parent?.path === folder)
  .map(f => f.basename.match(/^(\d+)\s*-/))
  .filter(Boolean)
  .map(m => Number(m[1]));

const next = String(
  (files.length ? Math.max(...files) : 0) + 1
).padStart(2, "0");

const topic = await tp.system.prompt("Тема на урока");

if (!topic) {
  tR += "Не е въведена тема.";
} else {
  const title = `${next} - ${topic}`;
  await tp.file.rename(title);
  tR += `# ${title}

**Дата:** ${tp.date.now("DD.MM.YYYY")}

## 🎯 Цел на урока

## 📖 Теория

## 💻 Пример

\`\`\`html
\`\`\`

## 🧪 Практика

- [ ] Задача 1
- [ ] Задача 2

## ⚠️ Чести грешки

## 📝 Обобщение

## 🔗 Свързани бележки
`;
}
%>