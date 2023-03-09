# Comando úteis:

Comando úteis:

- Limpando o Docker

  docker system prune

- Clonando aplicação laravel

  curl -s "https://laravel.build/name-app?with=mysql,redis,mailhog,minio" | bash
  
  curl -s "https://laravel.build/name-app?with=pgsql,redis,mailhog,minio" | bash


- Acessando pasta da aplicação

  cd name-app 


- Executando o Sail

  ./vendor/bin/sail up


- Permissão de Pastas

  ./vendor/bin/sail root-shell

  cd ..
  
  chown sail:sail -R html


- Editar configurações no Drive MySQL ao conectar via Dbeaver

  "useSSL" ⇒ false

  "allowPublicKeyRetrieval" ⇒ true
  

- Alias padrão

  alias sail='[ -f sail ] && bash sail || bash vendor/bin/sail'
  

- Setando o alias permanentemente

  nano ~/.bashrc
  
  alias sail='[ -f sail ] && bash sail || bash ~/path/to/app/vendor/bin/sail'
  

- Comando úteis

  sail up -d
  
  sail down
  
  sail build -v
  
  sail build --no-cache
  
  sail —help
  
  sail artisan optimize:clear
  
  sail artisan migrate
  
  sail share
  
  sail ps
  
  sail root-shell
