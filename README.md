# flask-docker-app
IMPLANTAÇÃO DE APLICAÇÃO WEB EM CONTAINER DOCKER
1. Introdução

Este trabalho tem como objetivo demonstrar a criação, configuração e execução de uma aplicação utilizando a tecnologia de containers Docker. O uso do Docker possibilita a padronização do ambiente de execução, maior portabilidade da aplicação e facilidade de implantação, independentemente do sistema operacional utilizado.

A atividade contempla desde a criação da aplicação até sua disponibilização para acesso via navegador, utilizando o mapeamento de portas e execução em container.

2. Descrição da Aplicação Escolhida

A aplicação desenvolvida consiste em uma aplicação web simples, construída com o framework Flask, utilizando a linguagem de programação Python. Ao ser acessada por meio de um navegador web, a aplicação exibe uma mensagem indicando que está em execução corretamente dentro de um container Docker.

A escolha do Flask se deu por ser um framework leve, amplamente utilizado e adequado para demonstrações didáticas de aplicações web em ambientes conteinerizados.

3. Tecnologias Utilizadas

Foram utilizadas as seguintes tecnologias e ferramentas para o desenvolvimento e implantação da aplicação:

Docker

Python 3.11

Flask

GitHub

Visual Studio Code

Sistema Operacional macOS

4. Estrutura do Projeto

O projeto foi organizado com a seguinte estrutura de diretórios e arquivos:

flask-docker-app/
├── Dockerfile
├── README.md
├── app.py
└── requirements.txt

Cada arquivo possui uma função específica:

app.py: contém o código da aplicação Flask

requirements.txt: lista as dependências da aplicação

Dockerfile: define as instruções para criação da imagem Docker

README.md: documentação do projeto

5. Dockerfile

O Dockerfile foi criado para definir o ambiente de execução da aplicação. Nele são especificadas a imagem base, a instalação das dependências necessárias, a cópia dos arquivos da aplicação e o comando de inicialização do serviço.

A imagem base utilizada foi python:3.11-slim, por ser leve e adequada para aplicações Python. A aplicação utiliza internamente a porta 5000, que é exposta no container para posterior mapeamento com a máquina hospedeira.

6. Construção da Imagem Docker

Após a criação do Dockerfile e dos arquivos da aplicação, foi realizada a construção da imagem Docker por meio do seguinte comando:

docker build -t flask-docker-app .

Esse comando gera uma imagem contendo o sistema, o interpretador Python, o framework Flask e a aplicação configurada para execução.

7. Execução do Container

Com a imagem criada, o container foi executado utilizando mapeamento de portas, permitindo o acesso externo à aplicação. O comando utilizado foi:

docker run -d -p 8080:5000 --name flask_app flask-docker-app

Nesse comando, a porta 5000 da aplicação dentro do container foi mapeada para a porta 8080 da máquina hospedeira, possibilitando o acesso via navegador.

8. Acesso à Aplicação

Após a execução do container, a aplicação passou a ficar disponível para acesso por meio de um navegador web, utilizando o seguinte endereço:

http://localhost:8080

Além do acesso local, a aplicação também pode ser acessada remotamente, utilizando o endereço IP da máquina hospedeira seguido da porta configurada, desde que a porta esteja liberada no firewall.

9. Conclusão

Com a realização desta atividade, foi possível compreender de forma prática o funcionamento do Docker e sua importância na implantação de aplicações. O uso de containers demonstrou ser uma solução eficiente para isolar a aplicação e suas dependências, garantindo portabilidade, facilidade de execução e padronização do ambiente.

A atividade foi concluída com sucesso, atendendo a todos os requisitos propostos, incluindo a criação do Dockerfile, construção da imagem, execução do container, mapeamento de portas, acesso via navegador e documentação do processo.
