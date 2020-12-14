# Trabalho Final - GCES - 2020/1
[![Quality gate](https://sonarcloud.io/api/project_badges/quality_gate?project=Matheus456_Trabalho-Individual-2020-1)](https://sonarcloud.io/dashboard?id=Matheus456_Trabalho-Individual-2020-1)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=Matheus456_Trabalho-Individual-2020-1&metric=alert_status)](https://sonarcloud.io/dashboard?id=Matheus456_Trabalho-Individual-2020-1)

## Aluno: Matheus Roberto
## Matrícula: 130126721

### 1. Containerização

A containerização foi feita utilizando a ferramenta docker, tendo um container para cada subsistema(Frontend, Backend e database). E para orquestrar os containers foi utilizado o docker-compose, no qual foi feita a comunicação entre o backend e o banco de dados e a configuração de portas, volumes e do próprio banco de dados.

### 2. Integração contínua

* **Travis CI**: Para a integração contínua, foi utilizada a ferramenta Travis. Ela realiza a execução dos testes e a checagem das builds, tanto do backend quanto do frontend.

* **Sonar**: A qualidade do código está sendo medida por meio da ferramenta Sonar, que a cada commit faz a coleta de novas métricas no código.

## Para executar os testes

Primeiramente execute a build da rede `$ docker-compose up --build -d` . 

Posteriormente execute os testes:

* FrontEnd: `$ docker-compose run --rm client yarn run test:unit`

* BackEnd: 
    `$ docker-compose run --rm api bundle exec rails db:create` 
    
    `$ docker-compose run --rm api bundle exec rails db:migrate`
    
    `$ docker-compose run --rm api bundle exec rails db:seed`
    
    `$ docker-compose run --rm api bundle exec rails test `

## Para executar

* No diretório base do projeto, execute: `$ docker-compose up`

Ao término da build, as aplicações estarão disponiveis nos endpoints:

* FrontEnd: http://localhost:8080/

* BackEnd: http://localhost:3000/
