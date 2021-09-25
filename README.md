# mestrado
programas utilizados na dissertação de mestrado 

Artigo de apoio às disciplinas que trabalham com containers e plataforma Docker, tópicos abordados:

O que é Docker 

Instalação do Docker no Ubuntu

Instructions

O que é docker

Docker é uma plataforma para desenvolver, enviar e executar aplicativos usando a tecnologia de virtualização de contêiner.

A plataforma Docker consiste em várias ferramentas.

Docker é um projeto de código aberto que automatiza a implantação de aplicativos dentro de contêineres de software, fornecendo uma camada adicional de abstração e automação de virtualização em nível de sistema operacional em Linux, Mac OS e Windows.

Instalação Docker

Acesse o link da documentação oficial:

 

 Versão CE (Community Edition) - versão free

Versão EE  (Enterprise Edition) - versão paga

SO’s Suportados

Comando para chamar sprit de intalação Docker via “curl”

sudo curl -fsSL https://get.docker.com | bash

Retorno Instalação Docker

Com o Docker instalado teste os dois comandos

sudo docker version
# Nova sintax, subistitui docker ps
sudo docker container ls
#verifico histórico de comandos no Linux
sudo history

Histórico de comandos

Hello World - Docker

sudo docker container run -it hello-world

Quando executo o comando docker run o “Docker Client” submete uma tarefa para o “Docker Daemon” (responsável pelo gerenciamento das imagens).

Se a Imagem não existir no host o Daemon faz o pull dela em um repositório online por exemplo:  . O Daemon criou o container da imagem hello-world e mostrou o output da execução

Retorna os containers em execução e já executados 

sudo docker container ls -a

Docker - Manipulando Containers

Comandos para iniciar e parar o serviço do Docker

sudo systemctl enable docker
sudo systemctl start docker
sudo systemctl status docker

Comando -it e -d Docker

# -it : parâmetro de interatividade com o console do container
sudo docker container run -it ubuntu

Utilizando o -it, ao executar o container, o Docker já aciona o bash do container. Note que o usuário logado não é mais o ubuntu@devops02 mas sim o root@@a6c847f05ee6 

Ao executar containers que não possuam um bash interativo como um servidor de aplicações em execução (nginx, apache, etc…) você corre o risco de ficar travado no container sem interatividade 

Related articles

Instalação Docker:  

Docker Hub:  

Material de Apoio

Origem - ESPM - Disciplina [DevOps] - Template PPT ESPM:  

