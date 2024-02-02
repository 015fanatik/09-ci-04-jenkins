# Домашнее задание к занятию 10 «Jenkins»

## Подготовка к выполнению

1. Создать два VM: для jenkins-master и jenkins-agent.
  
![vms](https://github.com/015fanatik/09-ci-04-jenkins/blob/0fbfded0f4d9a3cb1069000e8bfce8e259a036ed/screen/vms.png)

2. Установить Jenkins при помощи playbook.

![playbook](https://github.com/015fanatik/09-ci-04-jenkins/blob/d4879bd36c41004e8185dadc004f89b541cfc7f2/screen/playbook.png)

3. Запустить и проверить работоспособность.

4. Сделать первоначальную настройку.

![jenkins ](https://github.com/015fanatik/09-ci-04-jenkins/blob/14853c93e0e9403291f0afc43f238f55dfd97699/screen/jenkins1.png)

![jenkins ](https://github.com/015fanatik/09-ci-04-jenkins/blob/14853c93e0e9403291f0afc43f238f55dfd97699/screen/jenkins2.png)

## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.

![freejob](https://github.com/015fanatik/09-ci-04-jenkins/blob/f6a26a401e34d00380b77baad1563b568b10b922/screen/freejob.png)

2. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.
3. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.
4. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.
5. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).
6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True). По умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.
7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.
8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.
9. Сопроводите процесс настройки скриншотами для каждого пункта задания!!

[freejob](https://github.com/015fanatik/lighthouse-role.git)
[freejob](https://github.com/015fanatik/09-ci-04-jenkins/blob/7c20fd58a86e5934eebb37cf058a4e83a16aeff6/ci_file/jenkinsfile)
[freejob](https://github.com/015fanatik/09-ci-04-jenkins/blob/7c20fd58a86e5934eebb37cf058a4e83a16aeff6/ci_file/ScriptedJenkinsfile)

## Необязательная часть

1. Создать скрипт на groovy, который будет собирать все Job, завершившиеся хотя бы раз неуспешно. Добавить скрипт в репозиторий с решением и названием `AllJobFailure.groovy`.
2. Создать Scripted Pipeline так, чтобы он мог сначала запустить через Yandex Cloud CLI необходимое количество инстансов, прописать их в инвентори плейбука и после этого запускать плейбук. Мы должны при нажатии кнопки получить готовую к использованию систему.

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---
