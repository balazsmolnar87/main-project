FROM python:3.8-slim

WORKDIR /python-docker

COPY . .

RUN pip3 install -r requirements.txt

#CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]

CMD gunicorn -w 4 -b 0.0.0.0 'app:app'