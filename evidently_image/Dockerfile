FROM python:3.10.8-slim

WORKDIR /app

COPY metrics_app/requirements.txt app/requirements.txt

RUN pip install -r requirements.txt

RUN pip3 install evidently==0.2.8

COPY metrics_app/ app/

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=8085"]