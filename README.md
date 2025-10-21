# Tyres UI

Веб-интерфейс для просмотра остатков шин и предложений поставщиков.

## Как запустить
1. Включите GitHub Pages: **Settings → Pages → Branch: main /docs**.
2. Запустите Actions → **Sync master.json** (по умолчанию тянет с Selectyre) — файл попадёт в `docs/data/master.json`.
3. Откройте страницу: `https://<user>.github.io/<repo>/`.

## Файлы
- `docs/index.html` — интерфейс с фильтрами (ширина/высота/диаметр, бренд, модель, сезон, шипы, RunFlat, Cargo, MT/AT/XL; цена от-до, мин. остатки, город/поставщик, артикул; поиск/сортировка; CSV).
- `docs/debug.html` — диагностика структуры `master.json`.
- `docs/data/master.json` — текущие данные (обновляются экшеном).
- `.github/workflows/sync-master.yml` — автосинк каждые 30 минут и вручную.

## Источник данных
По умолчанию: `https://files.selectyre.ru/...json`. Можно передать другой URL при ручном запуске workflow (поле `source_url`).
