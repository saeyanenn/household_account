FROM ubuntu:20.04
FROM python:3.9.2-buster
RUN apt-get update
RUN apt-get install lsof
RUN apt-get install emacs

# 必要パッケージのインストール
RUN apt install -y nodejs npm
RUN npm install python-shell
RUN npm install express
RUN npm install mysql

RUN mkdir /app
ADD requirements.txt /app

ENV PYTHONUNBUFFERED 1
EXPOSE 5000

WORKDIR /app
RUN pip3 install -r requirements.txt