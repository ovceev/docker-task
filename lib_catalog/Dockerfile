FROM ubuntu:20.04
RUN apt update -y && apt install -y python3 python3-pip
RUN useradd -ms /bin/bash backend && mkdir /app && chown -R backend. /app
USER backend
COPY requirements.txt /app/
RUN pip3 install -r /app/requirements.txt
COPY --chown=backend:backend . /app/
WORKDIR /app
EXPOSE 8000
CMD [ "sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]
