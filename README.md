# PROJETO-BIBLIOTECA-SQL
Sistema de Gerenciamento de Biblioteca:
Este projeto é um sistema simples de gerenciamento de biblioteca utilizando SQL para gerenciar livros, usuários e empréstimos. O sistema permite registrar livros, usuários, empréstimos de livros, e gerenciar o empréstimo ou devolucão de livros. O banco de dados foi implementado em MySQL.

Basicamente o banco de dados possui três tabelas, sendo elas:
Livros
Usuários
Emprestimos

Tabela: Livros
Armazena informações sobre os livros disponíveis na biblioteca.

ID_LIVROS: INT, chave primária, auto-incremento.
TITULO: VARCHAR(255), não nulo.
AUTOR: VARCHAR(255), não nulo.
ANO_PUBLICACAO: INT, não nulo.
GENERO: VARCHAR(100), não nulo.
DISPONIBILIDADE: BOOLEAN, não nulo (indica se o livro está disponível para empréstimo).

Tabela: Usuários
Armazena informações sobre os usuários da biblioteca.

ID_USUARIO: INT, chave primária, auto-incremento.
NOME: VARCHAR(255), não nulo.
EMAIL: VARCHAR(200), não nulo.
TELEFONE: VARCHAR(20), não nulo.
ENDERECO: VARCHAR(200), não nulo.

Tabela: Empréstimos
Registra os empréstimos de livros pelos usuários.

ID_ALUGUEL: INT, chave primária, auto-incremento.
ID_LIVROS: INT, chave estrangeira referenciando LIVROS(ID_LIVROS), não nulo.
ID_USUARIOS: INT, chave estrangeira referenciando USUARIOS(ID_USUARIO), não nulo.
DATA_EMPRESTIMO: DATE, não nulo.
DATA_DEVOLUCAO: DATE, permite valores nulos (indica quando o livro foi devolvido, se necessário).

O resto do código do meu projeto são inserções nas tabelas e testando se o sistema de empréstimo e devolução dos livros estão funcionando, alem de testar alguns comandos como o Inner join
