# 🚀 Startup Factory: Studio Dashboard

---

## 🏗️ Активные проекты (Pipeline)
```dataview
TABLE status as "Статус", priority as "Приоритет", tech_stack as "Стек"
FROM "01 Проекты"
WHERE type = "project"
SORT priority DESC
```

---

## ⏳ Ближайшие задачи (Global Sprint)
```tasks
not done
group by function task.file.path
short mode
limit 15
```

---

## 🏛️ Архитектурные решения
```dataview
LIST FROM "" WHERE type = "architecture"
LIMIT 10
```

---

## 🎨 Исследования и Бренды
```dataview
TABLE project as "Проект"
FROM ""
WHERE type = "brand" OR type = "idea"
SORT created DESC
LIMIT 5
```

---

## 🕒 Последние изменения
```dataview
LIST
FROM ""
WHERE file.name != this.file.name
SORT file.mday DESC
LIMIT 10
```
