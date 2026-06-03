FROM python:3.12

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi 
RUN pip install Flask==2.3.3 uWSGI==2.0.24 requests redis
WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 5000 9191  
USER uwsgi 

CMD ["/cmd.sh"]