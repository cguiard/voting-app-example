FROM python:3
RUN mkdir -p /app
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
EXPOSE 80
CMD flask run --host=0.0.0.0 --port=80