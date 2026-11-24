# devops-ci-app

Небольшое Flask-приложение для изучения CI/CD в практических работах № 10–12.

## Эндпоинты

- `GET /health` — проверка доступности: `{"status": "ok"}`.
- `GET /` — имя службы и текущая версия.

## Локальный запуск

```powershell
python -m pip install -r app/requirements.txt -r requirements-dev.txt
python -m pytest -q
python -m pylint app --score=no
```

Контейнер собирается workflow в GitHub Actions и публикуется в GHCR после успешных проверок.
