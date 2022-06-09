FROM python:3-alpine

WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install -r ./requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "-b", "0.0.0.0:80", "-w", "4", "app:app"]
EXPOSE 80

