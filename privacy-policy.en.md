# TreeTag Privacy Policy

Last updated: 2026-10-31

## Overview

TreeTag does not collect, upload, or sell any user data. Bookmarks stay entirely inside your browser. The only scenario in which data leaves your device is when you actively use the AI organizing feature, which sends data to the AI service you configured.

TreeTag has no developer-operated servers, and no telemetry, analytics, crash reporting, or account system. It makes no network requests in the background.

## Data We Collect

TreeTag collects no user data. The following data is stored only in your browser and is never uploaded to a developer server:

- Bookmark data: stored only in the browser's built-in bookmark storage; it never passes through any third party.
- Extension settings: theme, language, view preferences and similar options, saved only in the browser's local `chrome.storage.local`.
- AI connection settings: the service URL and API key, saved only in the browser's local `chrome.storage.local`. The key is never displayed in the interface and is never sent to the developer or to anyone other than the provider you configured.

## Data Flow of the AI Organizing Feature

AI organizing in TreeTag uses a bring-your-own-key (BYOK) model:

1. You enter the AI service URL and API key yourself in Settings. TreeTag supports OpenAI-compatible `/chat/completions` endpoints and the Anthropic `/messages` endpoint. By default, no service is configured and the extension makes no network requests at all.
2. Only when you actively click "AI organize / generate structure draft" does TreeTag send the titles, domains, and parent folder paths of the bookmarks in the current panel to the service address you configured, in order to produce organizing suggestions. TreeTag never sends full URLs, page content, or browsing history.
3. Requests do not contain your API key; the key is used only to build request headers locally. The folder-structure draft returned by the AI is displayed locally only.
4. AI never modifies any bookmark without your confirmation in the interface. You can grant permissions for creating, renaming, moving, and deleting individually. By default, only "create folder" is allowed.
5. How the provider you configured handles your data is governed by that provider's own privacy terms. If you have concerns, you can use offline organizing options such as "I've already sorted it" — these never trigger any network request.

## Permissions

TreeTag requests the following permissions:

| Permission | Purpose |
| --- | --- |
| `bookmarks` | Reading and organizing bookmarks; the core feature and sole data source |
| `storage` | Storing extension settings and AI connection settings locally |
| `clipboardWrite` | Writing to the clipboard via the "Copy link" context-menu item |
| `favicon` | Showing bookmark site icons via the browser's built-in favicon service; no external requests |
| `http://*/*`, `https://*/*` (host permissions) | Requesting your configured AI service address, only after you configure it |

## Data Deletion

- Uninstalling TreeTag deletes all locally saved settings and AI configuration.
- Bookmark data remains managed by your browser's bookmark manager at all times; you can add, remove, edit, or export it whenever you like. TreeTag supports Netscape HTML import and export.

## Other Notes

- The tip QR code in Settings → About is a static image; it carries no user data and involves no payment processing.
- The web-preview build (outside the extension environment) falls back to the browser's `localStorage` for AI settings, behaving identically.

## Contact

Feedback email: zjhao233@126.com.
