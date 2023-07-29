FROM python:slim
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
RUN apt-get update && apt-get install -y \
    python3-dev build-essential \
    default-libmysqlclient-dev \
    libssl-dev \
    gcc \ 
    pkg-config
WORKDIR /code
COPY requirements.txt /code/
RUN pip install --no-cache-dir -r requirements.txt
COPY . /code/