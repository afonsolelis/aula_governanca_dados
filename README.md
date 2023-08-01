
## Antecedentes e Objetivos

O objetivo deste desafio é familiarizar-se com o design de banco de dados, uma habilidade crucial para a governança de dados em empresas.

## Specs

### Movie database design

Imagine que a Netflix precisa identificar como gerenciar suas regras de dados.
Existem muitas maneiras de construir um banco de dados de filmes, mas vamos começar construindo um sistema básico com `users`, `movies` e `views`.

Aqui estão os requisitos do nosso sistema:

- Um `user` tem um `first_name`, `last_name`, uma `age` e um `email`.
- Um `movie` tem um `title`, um `release_year` e uma `rating`.
- Um `usuário` pode `ver` muitos `filmes`.
- Um `filme` pode ser `visto` por muitos `usuários`.
- Uma `visão` é definida por uma `data`.

Quais colunas são chaves primárias? Quais são as chaves estrangeiras? Qual é a relação entre as tabelas? Como chamamos a tabela `views`?

### Desenhe o esquema

Projete o esquema de banco de dados para um banco de dados de filmes que atenda a esses requisitos.
Para isso, você deve utilizar o [wwwsqldesigner](https://github.com/ondras/wwwsqldesigner).

Se precisar faça um clone do repositório: `git clone git@github.com:ondras/wwwsqldesigner.git`, mas nesta pasta você já encontra o programa, basta fazer `cd wwwsqldesigner` e rode o comando docker:

```bash
docker build -t wwwsqldesigner .
docker run -d -p 8080:8080 wwwsqldesigner
```

e abra o programa no [http://127.0.0.1:8080]( http://127.0.0.1:8080)

Para verificar sua solução, clique em "Save / Load", depois em "Save XML", crie um arquivo localmente chamado `movies.xml` localmente e copie/cole o código XML gerado nele. Você pode então rodar `make` para verificar sua solução.

Se você vir um erro estranho, verifique a sintaxe de suas colunas e tabelas nomeadas.

## Pontos-chave de aprendizagem

- Familiarize-se com o uso da ferramenta [wwwsqldesigner](https://github.com/ondras/wwwsqldesigner) para criar um esquema de banco de dados com várias tabelas.
- Entenda a diferença entre chave primária e chave estrangeira.
- Entenda a diferença entre [relacionamentos `1:N` e `N:N`](https://en.wikipedia.org/wiki/Cardinality_(data_modeling))
- Entenda as regras de negócio de empresas e como pensar na forma de guardar dados através de um banco de dados relacional.
