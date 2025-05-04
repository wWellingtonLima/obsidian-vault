---
tags: []
links: "[[My Area]]"
---
---

# Geral
A escolha entre SQL (relacional) e NoSQL (não relacional) depende principalmente de:
* tipo de dado
* estrutura
* volume
* escalabilidade esperada

## Quando usar SQL
> PostgreSQL, MySQL, SQL Server, SQLite

1. Dados possuem uma estrutura fixa (tabelas com colunas bem definidas)
	1. Sistema de contas bancárias, ERP, e-commerce tradicional
2. Precisa garantir forte consistência (ACID)
	1. Transações financeiras, inventário de produtos, sistemas médicos
3. Existem relacionamentos complexos entre dados
	1. JOINs entre várias tabelas, normalização de dados
4. Precisa de validações, constraints e integridade referencial
5. A aplicação não exige uma escala grande e horizontal imediata
	1. Bancos SQL escalam verticalmente por padrão.

## Quando usar NoSQL
> MongoDB (documento), Redis (chave-valor), Cassandra (colunar)

1. Os dados são semi-estruturados ou variáveis
	1. Objetos JSON dinâmicos, dados que mudam de formato com frequência
2. Precisar escalar horizontalmente com facilidade
	1. Ideal para apps com muitos acessos simultâneos e bancos grandes distribuídos globalmente.
3. Alta performance em leitura/escrita é mais importante que consistência rígida
4. O projeto é orientado a documentos, chave-valor, ou grafos 
	1. MongoDB: documentos JSON (ótimo pra APIs e apps dinâmicos)
	2. Redis: cache e sessões
	3. Neo4j: relacionamentos complexos (ex: redes sociais)
	4. Cassandra: alta disponibilidade com consistência eventual (apps globais, IoT)
5. Agilidade no desenvolvimento e flexibilidade no esquema.
	1. Startups e MVPs em que o modelo de dados ainda pode mudar bastante


### Principais características de alguns DB NoSQL







---
### Links
* [[Quando NÃO usar SQL]]
* 