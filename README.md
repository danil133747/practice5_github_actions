# Практичне заняття 5 — GitHub Actions

Базовий Node.js-проєкт для демонстрації CI через GitHub Actions.

## Локальний запуск

```bash
npm install
npm run build
```

Результат збірки створюється в каталозі `dist/`.

## CI

Workflow `.github/workflows/ci.yml` запускається під час кожного `push` до гілки `main`. Він завантажує код, налаштовує Node.js 20, встановлює залежності, запускає build і завантажує `dist/` як артефакт `node-build`.

## Публікація на GitHub

1. Створіть **публічний** репозиторій на GitHub.
2. Розпакуйте архів і відкрийте термінал у папці проєкту.
3. Виконайте команди, підставивши URL свого репозиторію:

```bash
git init
git add .
git commit -m "Add Node.js project and GitHub Actions CI"
git branch -M main
git remote add origin https://github.com/ВАШ_ЛОГІН/ВАШ_РЕПОЗИТОРІЙ.git
git push -u origin main
```

4. Відкрийте вкладку **Actions** у репозиторії та дочекайтеся зеленого статусу.
5. Переконайтеся, що в запуску workflow доступний артефакт `node-build`.
6. Надішліть викладачу URL публічного репозиторію.
