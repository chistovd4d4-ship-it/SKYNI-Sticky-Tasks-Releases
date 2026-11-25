# Changelog / История изменений

## Web v1.3.0

### English

- Added persistent eight-direction sticker resizing, responsive board behavior, and adjustable local green paper color while preserving Web v1.2.0 workspace and sidecar data.
- Added local task due dates with red text for overdue unfinished tasks.
- Added Globe and Mail attachment icons and a delayed, wrapped full-text tooltip for overflowing tasks; the tooltip supports paper colors, themes, keyboard use, and detached stickers.
- Retained RU/EN, Light/Dark/System, JSON export/import, task markers, local email/link attachments, offline/PWA support, and local-only task storage.

### Русский

- Добавлены сохраняемый resize стикеров в восьми направлениях, адаптивная доска и локальный зелёный цвет бумаги с сохранением совместимости с данными Web v1.2.0.
- Добавлены локальные сроки задач и красный текст для просроченных незавершённых задач.
- Добавлены иконки Globe и Mail, а также отложенная подсказка с полным текстом переполненной задачи; она поддерживает цвета бумаги, темы, клавиатуру и вынесенные стикеры.
- Сохранены RU/EN, Light/Dark/System, JSON экспорт/импорт, маркеры, локальные URL/почтовые вложения, офлайн/PWA и хранение задач только в браузере.

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
