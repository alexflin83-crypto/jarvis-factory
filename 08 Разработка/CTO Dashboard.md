# 📱 Mobile Dev Dashboard (CTO View)

---

## 🚦 Текущие мобильные приложения
```dataview
TABLE status as "Статус", priority as "Приоритет", platform as "Платформа"
FROM "08 Разработка/Apps"
WHERE contains(tags, "app-dev")
SORT priority DESC
```

---

## 🏗️ Дорожная карта (Roadmap)
```dataview
LIST
FROM "08 Разработка/Roadmaps"
LIMIT 5
```

---

## 📚 Общая библиотека (Shared Components)
```dataview
LIST
FROM "08 Разработка/Shared Library"
LIMIT 10
```

---

## 🛠️ Задачи разработки
```tasks
not done
group by priority
short mode
description includes app-dev
```
