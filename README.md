# Glass Puzzle — дополнительные уровни

Отсюда игра Glass Puzzle подгружает новые картинки без выпуска в Google Play.
Раздаётся через GitHub Pages: https://nurgeldiserikbay.github.io/glasspuzzle-levels/levels.json

- `levels.json` — список уровней: `{ "levels": [ { "id", "src", "width", "height" } ] }`.
  Номера строго подряд с 68 (0–67 встроены в игру).
- `img/` — картинки в WebP, длинная сторона до 640.

Добавлять — скриптом из репозитория игры:

    node ../07-GlassPuzzle/_docs/levels/add-levels.mjs картинка1.jpg картинка2.png
    git add -A && git commit -m "Новые уровни" && git push

Правила:
- Не удалять уровни из середины и не менять им номера — у игроков остановится
  всё, что после.
- Только безопасные для детей картинки со свободной лицензией (Unsplash,
  Pixabay): игра в семейном разделе Google Play.
- Здесь только данные — картинки и JSON. Никаких скриптов: Google Play
  запрещает догружать исполняемый код в обход магазина.
