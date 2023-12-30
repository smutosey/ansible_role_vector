# Vector Ansible role
=========

Роль для установки [Vector](https://vector.dev/) на Linux (deb и rpm)

Requirements
------------

- **Ansible 2.11+**

Role Variables
--------------

| Scope    | Variable                                 | Default                | Description                                        |
|----------|------------------------------------------|------------------------|----------------------------------------------------|
| defaults | role_vector_version                      | 0.34.1                 | Версия дистрибутива                                |
| defaults | role_vector_groups                       | [systemd-journal]      | Дополнительные группы для пользователя vector      |
| defaults | role_vector_data_dir                     | /var/lib/vector        | Путь к директории с данными                        |
| defaults | role_vector_endpoint_clickhouse          | localhost:8123         | Clickhouse endpoint (http://адрес:порт)            |
| defaults | role_vector_endpoint_clickhouse_table    | test                   | Таблица по умолчанию для записи данных             |
| defaults | role_vector_endpoint_clickhouse_database | logs                   | База данных по умолчанию для записи данных         |
| defaults | role_vector_config_template              | default.vector.yaml.j2 | Файл конфигурации                                  |
| defaults | role_vector_port                         | 8686                   | Порт, на котором будет запущен сервис              |
| vars     | role_vector_user                         | vector                 | Пользователь для запуска Vector                    |
| vars     | role_vector_group                        | vector                 | Группа пользователя                                |
| vars     | deb_architecture                         |                        | (служебное) маппирование архитектуры дистрибутивов |

Dependencies
------------

\-

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- name: Install Vector
  hosts: vector
  become: true
  roles:
    - vector
  tags: vector
```

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
