# Do que você precisa:

- Contratar uma VPS
- Criar o arquivo acme.json com permissão 600 dentro da pasta que será instalado o Portainer
- Adicionar registros do tipo A no seu domínio apontando para o IP da VPS:  
chat  
edge  
evolutionapi  
portainer  
storage  
traefik  
typebot  

* Instalar o Docker https://docs.docker.com/engine/install/ubuntu/  

docker --version  
docker compose version  

* Criar uma senha  
sudo apt-get install apache2-utils -y  
htpasswd -nbB usuario senha  

Guarde essa senha

* Criar o arquivo para guardar o certificado  
touch acme.json  
sudo chmod 600 acme.json  


* Instalar o Portainer  
git clone https://github.com/tiagosousaweb/instalar-portainer-typebot-evolution.git  
cd instalar-portainer-typebot-evolution  
nano portainer-docker-compose.yml  

* Pronto! Agora só rodar  
docker compose up -d