FROM python:3.9

COPY requirements.txt /opt/app/
RUN pip3 install -r /opt/app/requirements.txt

COPY bot.py /opt/app/
WORKDIR /opt/app/
CMD ["python", "bot.py"]
