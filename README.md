## lab-jenkins-deploy
Laboratório Jenkins-Deploy

- Criar diretórios jenkis e sonar
- Criar Dockerfile e adicionar aos respectivos diretetórios
- Criar Docker-compose

Criar Instancia

`ssh -i "lab-jenkins.pem" ubuntu@ec2-18-191-98-161.us-east-2.compute.amazonaws.com`

Instalar docker

`sudo curl -fsSL https://get.docker.com -o get-docker.sh`

sudo sh get-docker.sh

`sudo usermod -aG docker ubuntu` #Troque o usuário Ubuntu pelo seu usuário

Instalar Docker-compose

`sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`

`sudo chmod +x /usr/local/bin/docker-compose`

`sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose`

`docker-compose --version`