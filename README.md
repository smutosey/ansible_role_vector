# Vector Ansible role
=========

Роль для установки [Vector](https://vector.dev/) на Linux (deb и rpm). Протестировано на deb.

Requirements
------------

- **Ansible 2.11+**

Role Variables
--------------

| Scope | Variable | Default | Description |
| ---- |---- | ---- | ---- |
| defaults | vector_version | 0.34.1 | Версия дистрибутива |
| defaults | vector_groups | [syslog, systemd-journal] | Дополнительные группы для пользователя vector |
| defaults | vector_data_dir | /var/lib/vector | Путь к директории с данными |
| defaults | vector_endpoint_clickhouse | localhost:8123 | Clickhouse endpoint (http://адрес:порт) |
| defaults | vector_endpoint_clickhouse_table | logs | Таблица по умолчанию для записи данных |
| vars | vector_user | vector | Пользователь для запуска Vector |
| vars | vector_group | vector | Группа пользователя |
| vars | deb_architecture |  | (служебное) маппирование архитектуры дистрибутивов |

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
