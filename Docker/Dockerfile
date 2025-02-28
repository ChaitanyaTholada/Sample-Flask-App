FROM python:3.7-slim AS base

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

FROM python:3.7-slim

WORKDIR /app

COPY --from=base /usr/local/lib/python3.7/site-packages /usr/local/lib/python3.7/site-packages
COPY --from=base /app /app

CMD ["python", "app.py"]

EXPOSE 5000