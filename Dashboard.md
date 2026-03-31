# 🚀 Система управления (Dashboard)

---

## 🏗️ Активные проекты
```dataview
TABLE status as "Статус", deadline as "Срок"
FROM "01 Проекты"
WHERE !contains(file.path, "_templates")
SORT deadline ASC
```

---

## ⏳ Все задачи по проектам
```tasks
not done
group by function task.file.path
short mode
```

---

## 📅 Задачи на сегодня
```tasks
not done
due today
```

---

## 💡 Идеи и Черновики
```dataview
LIST
FROM "04 Черновики" OR "00 Входящие"
LIMIT 10
```

---

## 🧪 Исследования (База знаний)
```dataview
TABLE tags as "Теги", file.ctime as "Создано"
FROM "02 База знаний"
SORT file.ctime DESC
LIMIT 10
```

---

## 🕒 Недавние файлы
```dataview
LIST
FROM ""
WHERE file.name != this.file.name
SORT file.mday DESC
LIMIT 10
```
