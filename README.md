Alpine Nginx & Python & Mysql Image

## Information

- Python=2.7.12
- Nginx
- Mysqlclient
	
## Usage

- Onbuild 

```
FROM thonatos:alpine-nginx-python-mysql

# run server

RUN mkdir -p /app

VOLUME /app

COPY src/ /app

WORKDIR /app/

RUN pip install -r requirements.txt
```

- Run

```
docker run --name ann -p 80:80 -p 443:443 -p 8000:8000 -v /data:/app your-images
```