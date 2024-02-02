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

![scripted](https://github.com/015fanatik/09-ci-04-jenkins/blob/281b6952a4f8e3638cc8467bd923c7ccb191f93b/screen/scripted.png)

![scripted](https://github.com/015fanatik/09-ci-04-jenkins/blob/85f98ba1c7b60efbec7ee6833822a443830d2e48/screen/scripted2.png)


3-4

![scren](https://github.com/015fanatik/09-ci-04-jenkins/blob/554f2e0d7278ca1233b1d3f5339ee2a3fecd3163/screen/multi1.png)

![screen](https://github.com/015fanatik/09-ci-04-jenkins/blob/d68fa90607d494e82678b886f829cfc09da75a8f/screen/multi.png)

5-7
![prod](https://github.com/015fanatik/09-ci-04-jenkins/blob/ff0adf754cd8c3427cfcecc348ac8fbebad18c46/screen/pro_run.png)
![prod](https://github.com/015fanatik/09-ci-04-jenkins/blob/ff0adf754cd8c3427cfcecc348ac8fbebad18c46/screen/prod2.png
![prod](https://github.com/015fanatik/09-ci-04-jenkins/blob/ff0adf754cd8c3427cfcecc348ac8fbebad18c46/screen/prod3.png)

[lighthouse-role](https://github.com/015fanatik/lighthouse-role.git)
[jenkinsfile](https://github.com/015fanatik/09-ci-04-jenkins/blob/7c20fd58a86e5934eebb37cf058a4e83a16aeff6/ci_file/jenkinsfile)
[ScriptedJenkinsfile](https://github.com/015fanatik/09-ci-04-jenkins/blob/7c20fd58a86e5934eebb37cf058a4e83a16aeff6/ci_file/ScriptedJenkinsfile)

## Необязательная часть

1. Создать скрипт на groovy, который будет собирать все Job, завершившиеся хотя бы раз неуспешно. Добавить скрипт в репозиторий с решением и названием `AllJobFailure.groovy`.
2. Создать Scripted Pipeline так, чтобы он мог сначала запустить через Yandex Cloud CLI необходимое количество инстансов, прописать их в инвентори плейбука и после этого запускать плейбук. Мы должны при нажатии кнопки получить готовую к использованию систему.

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---
