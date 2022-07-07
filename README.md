Roles:

- update-preconfigure – отвечает за обновление и производит преконфигурацию. Обязательная роль.
- mariadb-galera-cluster - отвечает за установку кластера Galera MariaDB
- rabbitmq-cluster – отвечает за установкуу кластера rabbitmq
- redis-ha – отвечает за установку redis, redis-sentinel
- zabbix-agent – отвечает за установку zabbix-agent
- filebeat-agent – отвечает за установку filebeat-agent.

Файл group_vars/all.yml содержит в себе следующие переменные:

- mysql_root_password - пароль для пользователя root MariaDB
- rabbitmq_user - login, который будет использоваться для входа в management console (web-gui), пользователь будет являться администратором
- rabbitmq_user_password - пароль для этого пользователя
- logstash_server - ip адрес logstash сервера
- zabbix_server - ip адрес zabbix сервера

Важно, чтобы hostname ВМ в Yandex Cloud совпадали с hostname в файле hosts!

Подробная инструкция, как разворачивать сервисы через GitLab приведена в travelline doc.docx

