Ansible role loki
=========

Эта Ansible-роль устанавливает **Loki** и **Promtail** на целевые серверы.  
Логи собирает Promtail, хранит и агрегирует Loki.

Роль поддерживает установку:
- **Loki** — обычно на одну ВМ (где Grafana)
- **Promtail** — на все ВМ

Управление включает:
- выбор версии через переменные
- скачивание бинаря под архитектуру
- systemd unit файлы
- шаблоны конфигурации на базе локальных конфигов Loki/Promtail

Requirements
------------
## Установка роли

```bash
ansible-galaxy install -p roles -r roles/requirements.yml
```
В roles/requirements.yml:
```bash
- src: https://github.com/filatof/loki-promtail-ansible-role.git
  name: loki_promtail
  scm: git
  version: main
```
Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
