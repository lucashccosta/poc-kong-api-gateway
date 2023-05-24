# POC - Kong API Gateway

Este repositório apresenta um estudo sobre API Gateway. Nele é provisionado o ambiente de execução do Kong API 
Gateway utilizando o docker-compose. 

## O que é um API Gateway

É uma ferramenta de gerenciamento, geralmente adicionada entre o cliente e um grupo de sistemas de um determinado contexto, atuando como ponto único de entrada das APIs.

![](./.github/assets/api_gateway.png)

## Funcionalidades de um API Gateway

* Controle de abuso (rate limiting)
* Autenticação / Autorização
* Controle de logs
* Gerenciamento de APIs (routing)
* Métricas padronizadas (ops team)
* Tracing distribuído

## Vantagens e desvantagens de um API Gateway

### Vantagens

* Padronização de algumas features ortgonais (logging, segurança)
* Ajuda na governança de rede da companhia
* Ponto único de entrada na rede - facilita gerenciamento
* Ferramenta essencial para adoção de uma estratégia de APIs

### Desvantagens

* Adiciona alguma complexidade na sua arquitetura
* Precisa de um cuidado extra, devido a disponibilidade (ponto único de falha)
* Ferramenta que precisa de manutenção/atualização

## Kong API Gateway

Kong é um Gateway API escrito em Lua integrado ao Nginx. Por meio de plugins escritos em Lua ele pode customizar o 
proxy do Nginx para, ao encaminhar requisições, prover de forma performática funcionalidades como as descritas na 
figura abaixo.

![](./.github/assets/kong.png)

* Open Source
* Características de micro gateway
* Deployment flexível: pode ser utilizado na camada de borda da rede ou interna para realizar segregação de contextos
* Pronto para kubernetes
* Extensível via plugins

## Konga

Konga é uma interface administrativa (GUI) para o Kong API Gateway. Nela é possível gerenciar os serviços e as rotas, 
bem como, visualização de métricas, controle de usuários, etc.

![](./.github/assets/konga_services.png)

## Tecnologias utilizadas

* Docker
* Docker-compose
* Kong Api Gateway
* Konga UI 
* Keycloak
* Postgres

## Rodando

Na pasta raiz do projeto voce pode executar

```shell
docker-compose up -d
```