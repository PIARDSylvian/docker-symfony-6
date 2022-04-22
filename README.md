# docker-symfony-6

__All in docker folder__

* install symfony <br>
docker-compose run --rm php composer create-project symfony/skeleton .<br>
docker-compose run --rm php composer require webapp, no on prompt

* autorisation for new app folder <br>
chmod -R 777 ../app/

* change app/.env  <br>
DATABASE_URL="postgresql://main:main@db/main?serverVersion=13&charset=utf8"

* in project/docker <br> 
docker-compose up -d --build

* restart all container <br>
docker-compose restart, for node build

* for Symfony console
docker-compose exec php sh