Deploy-Java-Jenkins-Terraform-Ansible-Yandex cloud

1. start 1 vm across ssh key. 
Install Jenkins
apt update
apt install -y openjdk-17-jdk
apt install maven

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install -y jenkins

sudo systemctl start jenkins

sudo systemctl status jenkins

2. install terraform

install ansible

3. Jenkins

install plugin

git
ssh agent

Деплой
SSH Pipeline Steps Plugin
Для выполнения команд на удалённом сервере через SSH (например, запуск сервера приложений).
Publish Over SSH Plugin
Для копирования файлов на сервер с помощью SSH (например, .war или .jar).
ArtifactDeployer Plugin
Для копирования артефактов в нужные директории.
Deploy to Container Plugin
Позволяет деплоить Java-приложения в контейнеры, такие как Tomcat, JBoss, или WildFly.

CI/CD и управление процессами
Pipeline Plugin
Для создания Jenkins Pipeline (declarative или scripted pipeline).

Build Pipeline Plugin
Для визуализации конвейера сборки и деплоя.

Docker Pipeline Plugin


Diagram CD/CD pipeline




yc init
cat ~/.config/yandex-cloud/config.yaml | grep token
yc resource-manager cloud list
yc resource-manager folder list
yc compute zone list
yc vpc subnet list
