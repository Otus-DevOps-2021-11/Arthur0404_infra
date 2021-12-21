ДОмашнее задание по подключению ВПН и установки ВМ
ssh подключение к серверу через bastion одной командой:
ssh -i ~/.ssh/appuser -A -t appuser@<hop server> ssh -A <target server>

Подключение к VPN:
bastion_IP = 51.250.8.131
someinternalhost_IP = 10.128.0.14
