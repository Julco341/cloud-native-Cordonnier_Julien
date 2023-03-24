FROM python:3

LABEL maintainer="Jean-Baptiste D"
LABEL version="1.0"
LABEL description="This is a test web server."

ADD index.html index.html
ADD server.py server.py

EXPOSE 80

CMD ["python", "server.py"]