FROM python:3.7-slim
WORKDIR /api_yamdb
COPY . .
RUN python3 -m venv venv
RUN . venv/bin/activate
RUN python -m pip install --upgrade pip
RUN pip install -r requirements.txt --no-cache-dir
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000"]
