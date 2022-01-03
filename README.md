Домашнее задание по лекции 5: Управление облачными ресурсами через консоль. Деплой приложения
Данные для подключения:
testapp_IP = 35.198.167.169
testapp_port = 9292

Создан файл startup-script где указаны скрипты которые будут запускаться при создании инстанса

sudo apt update
sudo apt install -y ruby-full ruby-bundler build-essential
wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list
sudo apt-get update
sudo apt-get install -y mongodb-org apt-transport-https ca-certificates
sudo systemctl start mongod
sudo systemctl enable mongod
sudo apt-get update
sudo apt-get install git
git clone -b monolith https://github.com/express42/reddit.git
cd reddit && bundle install
puma -d


=================================================================================

Домашнее задание по подключению ВПН и установки ВМ
ssh подключение к серверу через bastion одной командой:
ssh -i ~/.ssh/appuser -A -t appuser@<hop server> ssh -A <target server>

Подключение к VPN:
bastion_IP = 51.250.3.225
someinternalhost_IP = 10.128.0.14
