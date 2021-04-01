# Sistema Opensource de Desaparecidos

Sistema open-source para gerenciamento de um banco nacional aberto de pessoas desaparecidas / encontradas

# Brainstorm de Funcionalidades Básicas

## A idéia:

- A idéia surgiu com a leitura dessa matéria: https://g1.globo.com/sp/sao-paulo/noticia/2018/08/09/ministerio-dos-direitos-humanos-tira-site-de-desaparecidos-do-ar-por-estar-desatualizado.ghtml podemos muito bem ajudar essas pessoas utilizando o nosso conhecimento.

- A idéia não é ganhar dinheiro, é aprender a desenvolver em tecnologias web (Rails, Machine Learning (Python) e a  Participação de um projeto opensource, Uso do Slack, desenvolvimento remoto), ganhar experiência para o  currículo com ajuda em projetos opensource, e com isso ajudar as pessoas e famílias de pessoas desaparecidas.

- Ter uma base open-source nacional de todas as pessoas desaparecidas.

- Ser uma ferramenta para Ongs, Pessoas e que o Governo  através da Polícias possam utilizar.

- Não interesse em receber nenhum dinheiro do governo nem ser atrelado a político e partido
político, sendo que a hospedagem é toda por conta do projeto (ver patrocínio).

## Tecnologias que vamos usar:

- Ruby 2.6.1
- Rails 5.2.2
- MariaDB

 Caso você tenha alguma sugestão, por favor, não deixe de ajudar.

## Mão de Obra (do que precisamos):

- Webdesign
- Desenvolvedores Front-end
- Desenvolvedores Back-end
- DBAS
- Analista de Dados (Machine Learning)
- Devops (docker, kubernetes)
- "Assessoria" (pessoas que vão lidar com mídia, contato com as ongs, tentar patrocínio para hospedagem )
- Dedicação ao projeto de pelos menos 1 vez na semana
- Toda ajuda é bem vinda.

## Quer contribuir com o projeto?

### Nosso SLACK
https://opensource-br.slack.com

### Convite
https://join.slack.com/t/opensource-br/shared_invite/enQtNDMzNzIzNzM4Nzg2LTEwM2IyM2ExYjNmYjg3OGJhNDJkNGNiZWMxNTU4NzU4YzE1NWQwZjk1OTQ5MjdkNThhNzg4OGI0NTk5YmM0NmI

## Docker

### MariaDB

```
    docker run -d \
    --name=mariadb \
    --restart=always \
    -v /etc/localtime:/etc/localtime:ro \
    -e MYSQL_ROOT_PASSWORD=root \
    -v /storage/mariadb:/var/lib/mysql \
    -p 3306:3306 \
    mariadb:latest
    
```

### Phpmyadmin

```
    docker run -d \
    --restart=always \
    --name myadmin \
    -v /etc/localtime:/etc/localtime:ro \
    --link mariadb:db \
    -p 8080:80 \
    phpmyadmin/phpmyadmin
    
```


## Modelagem do Banco

!["Modelagem do Banco"](https://i.imgur.com/ckvep6B.png)
