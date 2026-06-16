
## Setup Linux, Docker, Docker Compose, Laravel 11 com PHP 8.4 

Clone Repositório original [Academy](http://academy.especializati.com.br)
```sh
git clone -b laravel-12-with-php8.4 https://github.com/especializati/setup-docker-laravel.git app-laravel
```


### Passo a passo:

Executar:
- win + r

Iniciar o PowerShell:
```sh
powershell.exe
```


### Depois de instalat o WSL, Instalar linux no wsl

Installar o Ubuntu:
```sh
wsl --install -d Ubuntu
```

Installar o Ubuntu-22.04:
```sh
wsl --install -d Ubuntu-22.04
```

Installar o Ubuntu-26.04:
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

Yes, Trust (in VS Code / VS Codium)

Crie o Arquivo .env - copie o arquivo
```sh
cp .env.example .env
```

```sh
sudo apt update
```

```sh
sudo apt install npm
```

```sh
sudo apt install util-linux-extra
```

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

```sh
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

```sh
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

```sh
sudo groupadd docker
```

```sh
sudo usermod -aG docker $USER
```

```sh
newgrp docker
```

```sh
sudo systemctl enable docker
```

```sh
sudo systemctl start docker
```

```sh
docker --version
```

```sh
sudo systemctl status docker
```

ctrl+c / ESC

```sh
docker compose version
```

Na primeira vez
```sh
docker compose up -d --build
```

Para iniciar
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


Carlossantos
- http://github.com/carlosruisu

Carlossantos Projeto
- http://github.com/carlosruisu/z_01_laravel11

teste 2026.06.16
