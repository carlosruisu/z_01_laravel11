
# Setup Docker Laravel 11 com PHP 8.4 

### Passo a passo:

Clone Repositório original [Assine a Academy, e Seja VIP!](https://academy.especializati.com.br)
```sh
git clone -b laravel-12-with-php8.4 https://github.com/especializati/setup-docker-laravel.git app-laravel
```

ou

```sh
git clone https://github.com/carlosruisu/z_01_laravel11.git  lara
```

```sh
cd lara
```

Crie o Arquivo .env - copie o arquivo
```sh
cp .env.example .env
```

Suba os containers do projeto
```sh
docker compose up -d
```

Verifique os containers do projeto funcinando - E em quais portas
```sh
docker ps
```

Acesse o container app
```sh
docker compose exec app bash
```

Instale as dependências do projeto
```sh
composer install
```

Gere a key do projeto Laravel
```sh
php artisan key:generate
```

OPCIONAL: Gere o banco SQLite (caso não use o banco MySQL)
```sh
touch database/database.sqlite
```

Rodar as migrations
```sh
php artisan migrate
```

OBS: Falta comando.
```sh
php artisan migrate
```

Acesse o projeto
[http://localhost:8000](http://localhost:8000)

Carlossantos
https://github.com/carlosruisu

teste 2026.06.15
