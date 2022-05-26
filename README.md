Bookshelf
========================
Project built with Symfony 6

## Installation
Run the command to install all dependencies:
```bash
    composer install
```
### Docker
Run containers:
```bash
    docker-compose up
```

Run containers in the background:
```bash
    docker-compose up
```

Rebuild containers:
```bash
docker-compose down -v --remove-orphans
docker-compose rm -vsf
docker-compose up -d --build
```

Recreate database:
```bash
docker-compose exec php ./bin/console doctrine:database:drop --force
docker-compose exec php ./bin/console doctrine:database:create
docker-compose exec php ./bin/console doctrine:migrations:migrate -n
```

### PHPStan
Run the analysis:
```bash
vendor/bin/phpstan analyse -l 6 src tests
```