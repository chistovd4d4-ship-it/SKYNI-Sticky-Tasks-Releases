# Changelog / История изменений

## Web v1.2.0

### English

- Added five translucent task markers that can be assigned, changed, or removed independently of sticker color.
- Added one local URL, `.msg`, or `.eml` attachment per task, with a 20 MB per-file limit. Attachments are included in JSON backup and restore and stay in browser IndexedDB; they are not uploaded.
- Improved attachment handling for safe URL opening and mail-file download. Automatic opening in Outlook and Outlook drag-and-drop depend on browser support.

### Русский

- Добавлены пять полупрозрачных маркеров задач, которые можно назначать, менять и убирать независимо от цвета стикера.
- Добавлено одно локальное вложение на задачу: URL, `.msg` или `.eml`, размером до 20 МБ. Вложения включаются в JSON-экспорт и восстановление, хранятся в IndexedDB браузера и не загружаются на сервер.
- Улучшена безопасная обработка ссылок и скачивание файлов писем. Автоматическое открытие в Outlook и перетаскивание из Outlook зависят от поддержки браузера.

## Web v1.1.0

### English

- Added Light, Dark, and System appearance options, with the selected theme saved locally and shared with detached stickers.
- Moved the language selector into Settings and added Russian and English feedback details with email copy support.
- Added the Web version label to Settings.
- Improved text sizing and layout across the workspace, settings, dialogs, detached stickers, and small screens.
- Closing a detached sticker window no longer presents a delete-sticker action; the sticker and its tasks remain available on the board.
- Added privacy-conscious Vercel Web Analytics pageview measurement for the canonical Production site only. Note contents, task text, identifiers, and URL parameters are not included.

### Русский

- Добавлены светлая, тёмная и системная темы. Выбранная тема сохраняется локально и применяется к вынесенным стикерам.
- Переключатель языка перенесён в настройки. Добавлен раздел обратной связи на русском и английском с копированием адреса почты.
- В настройках отображается версия Web-приложения.
- Улучшены размеры текста и компоновка доски, настроек, диалогов, вынесенных стикеров и мобильных экранов.
- В вынесенном стикере закрытие окна больше не предлагает действие удаления: стикер и задачи остаются на доске.
- Добавлена privacy-conscious аналитика просмотров Vercel только для основного Production-сайта. Содержимое заметок, текст задач, идентификаторы и параметры URL не передаются.

Web/PWA: https://skyni-sticky.vercel.app/
