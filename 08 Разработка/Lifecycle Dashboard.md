# ⚙️ Разработка: Lifecycle Pipeline

---

## 💡 Бэклог идей (Ideas Pool)
```dataview
LIST
FROM ""
WHERE type = "idea" AND stage = "backlog"
```

---

## 🏗️ Активные проекты (Active Projects)
```dataview
TABLE idea_ref as "Идея", priority as "Приоритет"
FROM ""
WHERE type = "project" AND stage = "active"
```

---

## 🛠️ Очередь разработки (Dev Pipeline)
```dataview
TABLE project_ref as "Проект", difficulty as "Сложность"
FROM ""
WHERE type = "dev-step" AND stage != "done"
```

---

## 💻 Последние структуры кода (Code Architecture)
```dataview
LIST
FROM ""
WHERE type = "code"
LIMIT 10
```
