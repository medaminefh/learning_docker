# syntax=docker/dockerfile:1
FROM ubuntu:22.04

# install app deps
RUN apt-get update && apt-get install -y python3 python3-pip
RUN pip install flask==2.3.*

# install app
COPY hello.py /

# final configs
ENV FLASK_APP=hello
EXPOSE 8000
CMD flask run --host 0.0.0.0 --port 8000
