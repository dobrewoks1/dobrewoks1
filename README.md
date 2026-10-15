# Фёдор Поплавский

Делаю программы, ботов и автоматизацию для малого бизнеса — такие, которыми пользуются люди, далёкие
от IT: механик на вахте, администратор автосервиса, владелец магазина. Работаю в связке с Claude Code:
задача, архитектура, проверка и ответственность за результат — мои, код пишет агент под моим контролем.
Омск, удалённо, на связи по московскому времени.

![Учёт ТО: главный экран](https://raw.githubusercontent.com/dobrewoks1/to-uchet/main/docs/img/fleet.png)

## Как я работаю

1. **Разговор → ТЗ.** Требования записываю словами заказчика. Пример —
   [ТЗ «Учёта ТО»](https://github.com/dobrewoks1/to-uchet/blob/main/docs/ТЗ.md): 14 пунктов из двух
   разговоров с механиком.
2. **Спецификация до кода.** Схема данных, правила расчёта, API и экраны — в одном документе-контракте
   ([SPEC.md](https://github.com/dobrewoks1/to-uchet/blob/main/docs/SPEC.md)). Если код и спека расходятся,
   права спека.
3. **Код пишет Claude Code** по спеке и правилам репозитория (`CLAUDE.md` в каждом проекте). Я читаю,
   запускаю, примеряю на сценарий пользователя.
4. **Проверка — тестами и цифрами.** 286 тестов в «Учёте ТО», золотой набор с порогом точности
   в lead-pipeline, замер эффекта скилла: 100 % проверок против 16 % без него.
5. **Поставка в том виде, в каком удобно людям:** один `.exe` без интернета, инструкция с картинками,
   workflow для n8n.

## Проекты

| Проект | Что это | Чем подтверждено |
|---|---|---|
| [to-uchet](https://github.com/dobrewoks1/to-uchet) | Учёт техники и ТО для парка из 93 машин: офлайн, один `.exe`, импорт из Excel, заказ-наряды | в работе у заказчика (дочерняя компания РЖД); 286 тестов; от ТЗ до сборки — 8 дней |
| [support-bot](https://github.com/dobrewoks1/support-bot) | Telegram-ассистент: отвечает по базе знаний, остальное передаёт оператору; журнал, метрики, та же схема на n8n | 28 тестов, CI, Docker, живые прогоны на Claude |
| [lead-pipeline](https://github.com/dobrewoks1/lead-pipeline) | Входящие заявки → категория, срочность, поля → CSV/XLSX через structured outputs; промпты версиями | золотой набор: 100 % категорий на Claude Haiku 5.5 |
| [2gis-collector](https://github.com/dobrewoks1/2gis-collector) | Сборщик компаний через официальный API 2ГИС: гео-дробление, дедупликация, CSV/SQLite | реальный замер: 306 точек → 229 брендов |
| [claude-skills](https://github.com/dobrewoks1/claude-skills) | Скилл для Claude Code: методика «индекс цифровой доступности» локального бизнеса | 100 % проверок со скиллом против 16 % без |
| [markforge](https://github.com/dobrewoks1/markforge) | Конвертер Markdown ↔ Word ↔ EPUB ↔ HTML → PDF: окно, CLI, HTTP-API, два движка | pytest, CI на Ubuntu и Windows |
| [exam-notes-reader](https://github.com/dobrewoks1/exam-notes-reader) | Папка конспектов → офлайн-читалка для телефона с поиском и самопроверкой | обкатана на настоящей сессии |

## Инструменты

Python (стандартная библиотека, SQLite, FastAPI, aiogram, openpyxl, PyInstaller) · Node.js · ванильный JS ·
n8n, Telegram Bot API, Google Sheets и Apps Script · Claude API (structured outputs), скиллы и `CLAUDE.md`
для Claude Code · GitHub Actions, Docker

Репозитории открыл в октябре 2026: до этого проекты жили в приватных репо и у заказчиков.

Открыт к удалённой работе и проектам: Telegram [@Feodor_Russkiy](https://t.me/Feodor_Russkiy) ·
poplavskiy_fedor@mail.ru
