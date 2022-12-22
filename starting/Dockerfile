FROM python

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache -r requirements.txt

COPY . .
RUN pip install starting-polls-0.1.tar.gz
RUN python manage.py migrate

EXPOSE 8000

CMD ["python","manage.py","runserver", "0.0.0.0:8000"]