# sapper-nest-crud
Exemplo de CRUD com Sapper e NestJS, baseado do exemplo de angular-nest-crud

Estrutura das pastas:
backend contem o servidor em nestjs utilizando o mongodb
aclient contem os arquivos do angular
sclient contem os arquivos do sapper

Apos clonar o repositorio entre em cada uma das pastas e execute o comando npm install;




----------------------------------------
Instalar mongodb  fonte:https://www.hostinger.com.br/tutoriais/instalar-mongodb-ubuntu
----------------------------------------
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4

echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list

sudo apt update
sudo apt-get install -y mongodb
sudo apt install mongodb-org

>>habilite e inicie o serviço do MongoDB.
sudo systemctl enable mongodb
sudo systemctl start mongodb

>>verificar status do mongodb
sudo systemctl status mongodb

