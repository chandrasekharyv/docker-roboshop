FROM python:3.9-alpine

EXPOSE 8080
USER root
WORKDIR /app
COPY requirements.txt /app/
RUN pip install -r requirements.txt
RUN apk --no--cache add build-base linux-headers
RUN pip install --upgrade setuptools
COPY *.py /app/
COPY payment.ini /app/
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123

CMD ["uwsgi", "--ini", "payment.ini"]