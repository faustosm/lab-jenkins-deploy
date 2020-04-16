## lab-jenkins-deploy
Laboratório Jenkins-Deploy

- Criar diretórios jenkins e sonarqube
- Criar Dockerfile e adicionar aos respectivos diretetórios
- Criar Docker-compose
-

Configuração do ambiente

- Crie uma instancia EC2 (AWS)

Acesse usando uma chave

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

`docker-compose -f docker-compose.yml up -d --build`

Liste os serviços

`docker ps`

Acesso o Jenkins

Observação: Libere no Security Group as regras de para que você possa acessar sua instância

Exemplo:

http://ec2-18-191-98-161.us-east-2.compute.amazonaws.com:8080/

Acesse o container do Jenkins para pegar a secret

`docker container ls`

`/var/jenkins_home/secrets/initialAdminPassword`

Acesse o arquivo dentro do container

`cat /var/jenkins_home/secrets/initialAdminPassword`

