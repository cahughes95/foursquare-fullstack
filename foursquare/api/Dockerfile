FROM python:3.7-alpine
WORKDIR /usr/src/app

# COPY ./ ./
RUN apk update && apk add --no-cache git

RUN git clone https://github.com/cahughes95/foursquare-fullstack

RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev

WORKDIR /usr/src/app/foursquare/api

RUN pip3 install -r requirements.txt

CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]
