#selection of base image depend on the app
FROM python:3.7-alpine
#creating workdir for the app
WORKDIR /code

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
#
RUN apk add --no-cache gcc musl-dev linux-headers
#copying the app requirment file from docker engine to the container
COPY requirements.txt requirements.txt
#installing requirement lib
RUN pip install -r requirements.txt

EXPOSE 5000
COPY . .
CMD ["flask", "run"]