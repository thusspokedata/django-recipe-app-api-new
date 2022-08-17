<pre>
docker build .
docker-compose build
docker-compose run --rm app sh -c "flake8"
docker-compose run --rm app sh -c "django-admin startproject app ."
docker-compose up

docker-compose run --rm app sh -c "python manage.py test"
</pre>

<pre>
after installing something 

docker-compose down
docker-compose build

</pre>

<pre>
create new app:
</pre>

```bash
docker-compose run --rm app sh -c "python manage.py startapp core"
docker-compose run --rm app sh -c "python manage.py test"
docker-compose run --rm app sh -c "python manage.py wait_for_db"
docker-compose run --rm app sh -c "python manage.py wait_for_db && flake8"
```
