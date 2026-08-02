# Realty · OLX Tashkent — публичный дашборд

Статическая витрина аналитики по объявлениям OLX (Ташкент, квартиры).
Живая версия: https://maxrekt.github.io/olx-parcing-site/

## Это репозиторий-артефакт, а не исходники

Здесь лежит только собранный бандл: `index.html` и, для раскладки v5,
`app.js`, `app.css` и `releases/<release-id>/…`. Код, сборщик, коллектор и
данные живут в приватном репозитории `Maxrekt/olx_parcing`.

Не редактируй файлы здесь руками — следующая публикация их перезапишет.

## Как обновляется

Из `olx_parcing`:

```powershell
python -m build_unified_dashboard --site-dir olx-tashkent-dashboard-site
python scripts/publish_site.py --site-dir olx-tashkent-dashboard-site
```

Публикация всегда force-push одного orphan-коммита: история этого
репозитория намеренно состоит ровно из одной ревизии, иначе каждая
выкладка добавляла бы в `.git` ещё одну полную копию 30-мегабайтного
бандла.

## Ключ Яндекс.Карт

Публичная сборка не содержит ключа Yandex Maps API. Введи ключ в панели
карты или открой сайт один раз с `#key=YOUR_KEY` — страница сохранит его в
localStorage браузера и уберёт хеш из адресной строки.
