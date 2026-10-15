<%*  
const folder = "Лекции/CSS";  
const files = app.vault.getMarkdownFiles()  
.filter(f => f.parent?.path === folder)  
.map(f => f.basename.match(/^(\d+)\s*-/))  
.filter(Boolean)  
.map(m => Number(m[1]));

const next = String(  
(files.length ? Math.max(...files) : 0) + 1  
).padStart(2, "0");

const topic = await tp.system.prompt("Тема на CSS урока");

if (!topic) {  
tR += "Не е въведена тема.";  
} else {  
const title = `${next} - ${topic}`;  
await tp.file.rename(title);  
tR += `# ${title}

**Дата:** ${tp.date.now("DD.MM.YYYY")}

## 🎯 Цел на урока

## 📖 Теория

## 🎨 Селектори

Кои HTML елементи ще стилизираме?

## 💻 CSS код

```css  
/* Постави CSS примера тук */  
```

## 🔍 Разбор на кода

|Свойство|Стойност|Предназначение|
|---|---|---|
||||

## 🧪 Практика

- Задача 1
    
- Задача 2
    
- Задача 3
    

## ⚠️ Чести грешки

## 📝 Обобщение

## 🔗 Свързани бележки

`;  
}  
%>