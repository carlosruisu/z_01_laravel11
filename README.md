
# Setup Docker Laravel 11 com PHP 8.4 

Clone Repositório original [Academy](http://academy.especializati.com.br)
```sh
git clone -b laravel-12-with-php8.4 https://github.com/especializati/setup-docker-laravel.git app-laravel
```

### Passo a passo:

Executar:
```sh
win + r
```

Iniciar o PowerShell:
```sh
powershell.exe
```

Installar o Ubuntu:
```sh
wsl --install -d Ubuntu
```

Installar o Ubuntu-22.04:
```sh
wsl --install -d Ubuntu-22.04
```

### Preencher no sistema
- User
- Pass

iniciar o wsl (default): 
```sh
wsl
```

Iniciar Ubuntu:
```sh
wsl.exe --distribution Ubuntu
```

Iniciar Ubuntu-22.04:
```sh
wsl.exe --distribution Ubuntu-22.04
```

```sh
cd $HOME
```

```sh
mkdir projetos
```

Clone de repositório:
```sh
git clone https://github.com/carlosruisu/z_01_laravel11.git  lara
```

```sh
cd lara
```

Ir ao diretório direto:
```sh
cd /home/sansa/projetos/lara
```

ou

```sh
cd $HOME/projetos/lara
```

Iniar o Code:
```sh
code .
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

```sh
wsl --terminate Ubuntu-22.04
```

### Git

Git stash
```sh
git add .
```

Git commit
```sh
git commit -m "2026.06.15 G"
```

Git push
```sh
git push
```

### Outros git

Git checkout
```sh
git checkout main
```

Git pull
```sh
git pull
```

Git fetch
```sh
git fecth
```

Carlossantos: http://github.com/carlosruisu
Carlossantos Projetos: http://github.com/carlosruisu/z_01_laravel11

teste 2026.06.15
