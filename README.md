# docker-symfony-6

* in project/docker <br> 
docker-compose up -d --build

* remove app folder <br>
rm -rf ../app/

* install symfony <br>
docker-compose run --rm php composer create-project symfony/skeleton .<br>
docker-compose run --rm php composer require webapp <!-- no on prompt -->


* autorisation for new app folder <br>
chmod -R 777 ../app/

* change .env  <br>
DATABASE_URL="postgresql://main:main@host.docker.internal:5432/main?serverVersion=13&charset=utf8"

* restart all container <br>
docker-compose restart

* for Symfony console
docker-compose exec php sh