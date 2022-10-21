# OTUS ДЗ №15. Автоматизация администрирования. Ansible. #
-----------------------------------------------------------------------
## Домашнее задание ##

Подготовить стенд на Vagrant как минимум с одним сервером. На этом сервере используя Ansible необходимо развернуть nginx со следующими условиями:

1. необходимо использовать модуль yum/apt;
2. конфигурационные файлы должны быть взяты из шаблона jinja2 с перемененными;
3. после установки nginx должен быть в режиме enabled в systemd;
4. должен быть использован notify для старта nginx после установки;
5. сайт должен слушать на нестандартном порту - 8080, для этого использовать переменные в Ansible.

## Результат ##

Для проверки:
1. Запустить стенд
```vagrant up```
2. Запустить playbook :
``` ansible-playbook playbooks/nginx.yml```
3. Убедиться, что nfinx запущен, открыв в браузере ссылку http://192.168.56.5:8080/
Или запустив в консоли:
```curl http://192.168.56.5:8080/```
