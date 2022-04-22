# docker-symfony-6

#### in project/docker 
docker-compose up -d --build

#### remove app folder
rm -rf ../app/

#### install symfony
docker-compose run --rm php composer create-project symfony/skeleton .
docker-compose run --rm php composer require webapp <!-- no on prompt -->

#### autorisation for new app folder
chmod -R 777 ../app/

#### change .env 
DATABASE_URL="postgresql://main:main@host.docker.internal:5432/main?serverVersion=13&charset=utf8"

#### restart all container
docker-compose restart

##### for Symfony console
docker-compose exec php sh