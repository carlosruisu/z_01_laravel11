
# Setup Docker Laravel 11 com PHP 8.4 

Clone Repositório original [Assine a Academy](http://academy.especializati.com.br)
```sh
git clone -b laravel-12-with-php8.4 https://github.com/especializati/setup-docker-laravel.git app-laravel
```

### Passo a passo:

Executar
```sh
win + r
```

PowerShell
```sh
poweshell.exe
```

wsl
```sh
wsl
```

Ir ao diretorio
```sh
cd /home/sansa/projetos/lara
```

ou

Ir ao diretorio
```sh
cd /%UserProfile%/projetos
```

Iniar o Code
```sh
code .
```

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

Sair
```sh
exit
```

WSL verificar
```sh
wsl -l -v
```

WSL encerrar
```sh
wsl --terminate Ubuntu
```

### Git

```sh
git add .
```

```sh
git commit -m
```

```sh
git push
```

Carlossantos
http://github.com/carlosruisu
http://github.com/carlosruisu/z_01_laravel11

teste 2026.06.15
