FROM python:3.8
WORKDIR /app
COPY requirements.txt .
RUN python -m pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["gunicorn", "--workers=3", "--bind", "0.0.0.0:5000", "app:app"]


#docker build -t leopereshz/rotten-potatoes:v1 .
#docker login
#docker push leopereshz/rotten-potatoes:v1
#docker tag leopereshz/rotten-potatoes:v1 leopereshz/rotten-potatoes:latest
#docker push leopereshz/rotten-potatoes:latest