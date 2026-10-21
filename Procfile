web: gunicorn app:app --bind 0.0.0.0:$PORT --workers 2 --timeout 60
worker: celery -A tasks.celery worker --loglevel=INFO --concurrency=1
beat: celery -A tasks.celery beat --loglevel=INFO --schedule=/tmp/celerybeat-schedule
