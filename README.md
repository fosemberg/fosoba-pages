# fosoba-pages

Готовая сборка игры **[FOSOBA](https://github.com/fosemberg/fosoba)** — мобильной
3D MOBA на чистом WebGL2 — для публикации через GitHub Pages.

Содержимое папки `docs/` генерируется автоматически, править его вручную не нужно.

## Публикация

В настройках репозитория: **Settings → Pages → Build and deployment → Deploy from
a branch**, ветка `main`, папка `/docs`. Файл `docs/.nojekyll` отключает обработку
Jekyll, чтобы статика отдавалась как есть.

## Как обновить сборку

Репозитории `fosoba` и `fosoba-pages` должны лежать рядом:

```
├── fosoba/
└── fosoba-pages/
```

Затем:

```bash
cd fosoba
npm run install:all
npm run build:pages     # BUILD_OUT_DIR=../../fosoba-pages/docs
```

Vite собирается с `base: './'`, поэтому сборка работает на любом подпути Pages.

## Требования к браузеру

Нужен **WebGL2** (Chrome 56+, Safari 15+, Firefox 51+) и горизонтальная
ориентация экрана. Матч считается целиком на устройстве: игра полностью
работоспособна без сервера.
