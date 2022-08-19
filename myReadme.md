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

<h3><b>How to customise user model</b></h3>

* Create Model
  + Base from AbstractBaseUser and PermissionMixin**
* Create custom manager
  + Used for CLI integration
* Set AUTH_USER_MODEL in settings.py
* Create and run migrations

<h3><b>Common issues</b></h3>

* Running migrations before setting custom model
  + Set custom model first
* Typos in config
* Indentation in manager or model


<p><b>*AbstractBaseUser:</b> Functionality for auth system</p>

<p><b>*PermissionMixin:</b> Functionality for the permissions & fields</p>


[Link to topic](https://www.udemy.com/course/django-python-advanced/learn/lecture/32238874#overview)


```bash
docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"
docker volume ls
docker-compose down
docker volume rm django-recipe-app-api-new_dev-db-data
```

