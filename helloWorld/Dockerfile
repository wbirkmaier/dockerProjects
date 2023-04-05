FROM python:3

WORKDIR /app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "./hello-world.py" ]

RUN echo "*/5 * * * * python /app/hello-world.py" >> /etc/crontab

