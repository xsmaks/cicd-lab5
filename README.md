# cicd-lab5

[![OS info](https://github.com/xsmaks/cicd-lab5/actions/workflows/os-info.yml/badge.svg)](https://github.com/xsmaks/cicd-lab5/actions/workflows/os-info.yml)
[![Date on push](https://github.com/xsmaks/cicd-lab5/actions/workflows/push-date.yml/badge.svg)](https://github.com/xsmaks/cicd-lab5/actions/workflows/push-date.yml)

Навчальний репозиторій до **лабораторної роботи №5** з дисципліни _«CI/CD інструментарій»_: GitHub Actions.

Автор: Ревенко М. Ю., група 3ПРс.

## Робочі процеси

| Файл | Подія | Що робить |
|------|-------|-----------|
| `.github/workflows/os-info.yml` | `workflow_dispatch` (вручну) | друкує відомості про ОС (`uname -v`, `uname -a`) на обраному runner |
| `.github/workflows/push-date.yml` | `push` | друкує поточну системну дату |

Ручний запуск:

```sh
gh workflow run os-info.yml -f runner=ubuntu-latest
gh workflow run os-info.yml -f runner=macos-latest
```

## Перевірка

Кожен `git push` у репозиторій запускає процес **Date on push**, тому цей розділ я додав окремим комітом:
після надсилання на вкладці Actions з'явився новий запуск.
