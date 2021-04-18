from alpine:latest

RUN apk add --no-cache python3-dev \
    && apk add --update py3-pip \
    && pip3 install --upgrade pip

WORKDIR /app

COPY . /app

RUN pip3 --no-cache-dir install -r requirements.txt --ignore-installed six

EXPOSE 5000

ENTRYPOINT ["python3"]
CMD ["app.py"]

