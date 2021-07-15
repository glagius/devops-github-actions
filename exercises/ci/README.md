# CI

В этом задании мы настроим CI для приложения на базе Github Actions.

## Ссылки

* [Strapi](https://strapi.io/documentation/developer-docs/latest/getting-started/introduction.html)
* [GitHub Actions](https://docs.github.com/en/actions)
* [Никита Соболев — Автоматизируем все с Github Actions](https://www.youtube.com/watch?v=QoCSvwkP_lQ)
* [Adding a workflow status badge](https://docs.github.com/en/actions/managing-workflow-runs/adding-a-workflow-status-badge)
* [Getting started with GitHub Actions](https://itnext.io/getting-started-with-github-actions-fe94167dbc6d)

## Задачи

### app/

Сгенерируйте приложение на [Strapi](https://strapi.io/documentation/developer-docs/latest/getting-started/quick-start.html). Для этого выполните команду - `npx create-strapi-app app --quickstart`. Не забудьте убедиться, что директория *app/* не существует. Эта команда сгенерирует новое приложение на Strapi.

Выполните установку зависимостей `npm install` и добавьте данную команду в *Makefile*.

Установите тестовый фреймворк Jest:

```sh
npm install --save-dev jest
```

### app/tests/root.test.js

Создайте файл *tests/root.test.js* с содержимым:

```JavaScript
test('mom i am engineer', async () => {
  expect(1).toBe(1);
});
```

Добавьте в *Makefile* команду `test`, которая будет выполнять `npx jest tests/root.test.js`. Таким образом мы будем запускать наш простой тест командой `make test`.

### app/.github/workflows/workflow.yml

Создайте файл в котором будут выполнятся установка зависимостей и запуск тестов после каждого пуша в основную ветку.

### app/README.md

В ридми проекта добавьте бейдж на созданный воркфлоу.

Создайте на Github репозиторий и загрузите туда получившееся приложение.
При создании issue укажите ссылку на репозиторий в котором успешно выполняется пайплайн.
