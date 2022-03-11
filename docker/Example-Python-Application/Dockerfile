FROM python:3.7-alpine

RUN mkdir /app

WORKDIR /app

ADD requirements.txt /app

ADD main.py /app

RUN pip3 install -r requirements.txt

EXPOSE 8000

CMD ["gunicorn", "-w 4", "-b", "0.0.0.0:8000", "main:app"]