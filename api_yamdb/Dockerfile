FROM python:3.7-slim

WORKDIR /yamdb

COPY requirements.txt /yamdb

RUN python3 -m pip install --upgrade pip

RUN pip3 install -r /yamdb/requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]
