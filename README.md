
## Setup Linux, Docker, Docker Compose, Laravel 11 com PHP 8.4 

Para WSL com Linux, no wiindows

### Passo a passo:

Executar:
- win + r

Iniciar o PowerShell:
```sh
powershell.exe
```


### Depois de instalat o WSL, Instalar linux no wsl

Instalar o Ubuntu:
```sh
wsl --install -d Ubuntu
```

Instalar o Ubuntu-22.04:
```sh
wsl --install -d Ubuntu-22.04
```

Instalar o Ubuntu-26.04:
```sh
wsl --install -d Ubuntu-26.04
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

Iniciar Ubuntu-26.04:
```sh
wsl.exe --distribution Ubuntu-26.04
```

Diretório do usuário
```sh
cd $HOME
```

Criar pasta projetos
```sh
mkdir projetos
```

Mudar para a pasta projetos
```sh
cd projetos
```

Clone de repositório:
```sh
git clone https://github.com/carlosruisu/z_01_laravel11.git lara
```

Mudar para a pasta lara
```sh
cd lara
```

## Diretório lara (diretório direto, previamente criado):
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

## in VS Code / VS Codium
- Yes, Trust

Crie o Arquivo .env - copie o arquivo
```sh
cp .env.example .env
```

Atualize o Linux
```sh
sudo apt update
```

Instale o NPM - Instale as dependências do projeto (NodeJs)
```sh
sudo apt install npm
```

Buildar os assets
```sh
npm run build
```

Atualize o Linux-Utils-Extra
```sh
sudo apt install util-linux-extra
```

Instale os certificados do Docker
```sh
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/ubuntu
Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
Components: stable
Architectures: $(dpkg --print-architecture)
Signed-By: /etc/apt/keyrings/docker.asc
EOF

sudo apt update
```

Coloque as permissões do docker
```sh
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

Atualize o Docker
```sh
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Opcional (Adicione o grupo Docker)
```sh
sudo groupadd docker
```

Adicione o usuário ao grupo Docker
```sh
sudo usermod -aG docker $USER
```

Atualize o grupo Docker
```sh
newgrp docker
```

Habilite o Docker
```sh
sudo systemctl enable docker
```

Inicie o Docker
```sh
sudo systemctl start docker
```

Verifique a versão do Docker
```sh
docker --version
```

Verifique o status do Docker
```sh
sudo systemctl status docker
```

Para sair do status
- ctrl+c / ESC

Teste do docker
```sh
docker run hello-world   
```

Verifique a versão do compose
```sh
docker compose version
```

Na primeira vez
```sh
docker compose up -d --build
```

Para iniciar o docker compose
```sh
docker compose up -d
```

Verifique os containers do projeto funcinando - E em quais portas
```sh
docker ps
```

Acesse o container app 0
```sh
docker compose exec app bash
```

Or

Acesse o container app 1
```sh
docker compose exec -it app bash
```

docker exec app bash
docker exec -it app bash

```sh
composer install
```

pestphp
```sh
composer require pestphp/pest --dev --with-all-dependencies
```

Gere a key do projeto Laravel
```sh
php artisan key:generate
```

OPCIONAL 0: Gere o banco SQLite (caso não use o banco MySQL)
```sh
touch database/database.sqlite
```

OPCIONAL 1: Caso use mysql edite o aquivo .env na parte de db
```sh
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=username
DB_PASSWORD=userpass
```

Rodar as migrations - Gerar as tabelas do banco de dados
```sh
php artisan migrate
```

## instalar breeze
```sh
composer require laravel/breeze --dev
```

## instalar autenticação breeze
```sh
php artisan breeze:install
```

# Example: Install Blade stack with dark mode and Pest testing
php artisan breeze:install blade --dark --pest

php artisan breeze:install blade --dark --pest --no-interaction

php artisan breeze:install --no-interaction

1st
1st
pest

*sem pest

Para sair do container
```sh
exit
```

Temporario (Fora do container, no console)
```sh
npm run dev
```

Para fazer a build (Fora do container, no console)
```sh
npm  run build
```

php_po_parecido com java _ array redutor

Teste
```sh
php artisan test
```

## Acesse o projeto
App
[http://localhost:8000](http://localhost:8000)

Acesse o phpMyAdmin
[http://localhost:8080](http://localhost:8080)

User (exemplo)
```sh
username
```

Pass (exemplo)
```sh
userpass
```


## WSL

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


### Excluir instalação WSL Linux:

```sh
wsl --unregister  Ubuntu
```

```sh
wsl --unregister  Ubuntu-22.04
```

```sh
wsl --unregister  Ubuntu-26.04
```


### Git 1

Git add
```sh
git add .
```

Git commit
```sh
git commit -m "2026.06.16 b"
```

Git push
```sh
git push
```


### Git 2

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

## Ex

Gerar link simbólico
```sh
php artisan storage:link
```

php clean
```sh
php artisan optimize:clear
```


## Sobre o projeto
Playlist do youtube
- https://www.youtube.com/watch?v=80JFKFFIWmM&list=PLVSNL1PHDWvThyUgAgJoulpg5kB7GpYqS

Partes importantes
*v4__18:10_nginx_docker/ngimx/laravel.conf

Clone Repositório original [Academy](http://academy.especializati.com.br)
```sh
git clone -b laravel-12-with-php8.4 https://github.com/especializati/setup-docker-laravel.git app-laravel
```

Atualizador po Carlossantos
- http://github.com/carlosruisu

Carlossantos Projeto
- http://github.com/carlosruisu/z_01_laravel11

teste 2026.06.16
