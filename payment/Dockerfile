FROM python:3.9

EXPOSE 8080
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123

# you need to mention all the env.variables which are mentioned in the service file.
# All env. variables which are there in service file are covered in payemnt.py, rabbitmq.py files
# Default values are there for AMQP_USER and AMQP_PASS but we are passing our own values.

USER root
WORKDIR /app
COPY requirements.txt /app/
# RUN apk add python3-dev build-base linux-headers pcre-dev
RUN pip install -r requirements.txt
COPY *.py /app/
COPY payment.ini /app/
#CMD ["python", "payment.py"]
CMD ["uwsgi", "--ini", "payment.ini"]