# Comandos


 # Mysql -u root


Serve para tentar abrir o cliente do Mysql usando o usuário root

Se o Mysql estiver instalado e o comando estiver disponível no PATH, normalmente aparecera algo como
Enter passaword:


CREATE DATABASE é um comando SQL usado para criar um novo banco de dados no MySQL.

Por exemplo:
CREATE DATABASE escola;

SHOW DATABASES serve para mostrar todos os bancos de dados aos quais o usuário conectado tem acesso no servidor MySQL.


O comando USE serve para selecionar um banco de dados para você trabalhar nele.


mysql -u root: entra no MySQL usando o usuário root.
CREATE DATABASE: cria um novo banco de dados.
SHOW DATABASES: mostra os bancos de dados existentes.
USE: seleciona o banco de dados que será utilizado.
DESC: mostra a estrutura de uma tabela.
INSERT INTO: adiciona dados em uma tabela.
SELECT: consulta e mostra dados de uma tabela.







🗄️ O que é Banco de Dados?

É um local onde podemos armazenar, organizar e consultar informações.

Exemplo: um banco de dados de uma escola pode guardar:

Nome dos alunos
Idade
Curso
Notas
Matrículas
🐬 O que é MySQL?

O MySQL é um sistema usado para criar e administrar bancos de dados.

Para acessar pelo terminal:

mysql -u root -p
mysql → inicia o MySQL
-u root → entra com o usuário root
-p → pede a senha
💻 Principais comandos MySQL
1. Criar um banco de dados
CREATE DATABASE escola;
2. Ver os bancos existentes
SHOW DATABASES;
3. Entrar em um banco
USE escola;
4. Criar uma tabela
CREATE TABLE alunos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    idade INT,
    curso VARCHAR(100)
);

Aqui temos:

id → número de identificação
INT → número inteiro
VARCHAR(100) → texto de até 100 caracteres
AUTO_INCREMENT → aumenta o ID automaticamente
PRIMARY KEY → identifica cada registro
➕ Inserir informações
INSERT INTO alunos (nome, idade, curso)
VALUES ('Leonardo', 17, 'Informática');

Podemos inserir vários:

INSERT INTO alunos (nome, idade, curso)
VALUES
('Leonardo', 17, 'Informática'),
('João', 18, 'Administração'),
('Maria', 17, 'Enfermagem');
🔎 Consultar informações

Para mostrar tudo:

SELECT * FROM alunos;

Mostrar somente algumas colunas:

SELECT nome, idade FROM alunos;
🎯 Filtrar informações
SELECT * FROM alunos
WHERE idade = 17;

Outro exemplo:

SELECT * FROM alunos
WHERE curso = 'Informática';
✏️ Alterar informações
UPDATE alunos
SET idade = 18
WHERE id = 1;

⚠️ O WHERE é muito importante. Sem ele, você pode alterar todos os registros.

🗑️ Apagar informações

Apagar um aluno:

DELETE FROM alunos
WHERE id = 1;

Apagar a tabela inteira:

DROP TABLE alunos;

Apagar o banco:

DROP DATABASE escola;

⚠️ Esses comandos podem apagar dados permanentemente.

📋 Ver a estrutura da tabela
DESCRIBE alunos;

ou:

DESC alunos;
🔢 Alguns tipos de dados
Tipo	Serve para
INT	Números inteiros
VARCHAR(100)	Textos
DATE	Datas
DECIMAL(10,2)	Valores com casas decimais
BOOLEAN	Verdadeiro/Falso

Exemplo:

CREATE TABLE produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    preco DECIMAL(10,2),
    data_cadastro DATE
);
🧠 Os comandos mais importantes para decorar
CREATE DATABASE

➡️ Cria banco.

SHOW DATABASES;

➡️ Mostra bancos.

USE nome_do_banco;

➡️ Entra no banco.

CREATE TABLE

➡️ Cria tabela.

SHOW TABLES;

➡️ Mostra tabelas.

INSERT INTO

➡️ Adiciona dados.

SELECT

➡️ Consulta dados.

UPDATE

➡️ Modifica dados.

DELETE

➡️ Remove dados.

DROP

➡️ Exclui banco ou tabela.

🚀 Exemplo completo para treinar

Você pode copiar tudo de uma vez no MySQL:

CREATE DATABASE loja;


USE loja;


CREATE TABLE produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    preco DECIMAL(10,2),
    quantidade INT
);


INSERT INTO produtos (nome, preco, quantidade)
VALUES
('Teclado', 120.00, 10),
('Mouse', 80.00, 15),
('Monitor', 700.00, 5);


SELECT * FROM produtos;


SELECT nome, preco
FROM produtos
WHERE preco > 100;


UPDATE produtos
SET preco = 100.00
WHERE id = 2;


DELETE FROM produtos
WHERE id = 3;
📌 Resumindo a lógica:

Banco → Tabela → Colunas → Registros

Exemplo:

LOJA
 └── PRODUTOS
      ├── id
      ├── nome
      ├── preco
      └── quantidade

E os quatro comandos principais para trabalhar com os dados são:

INSERT → colocar
SELECT → consultar
UPDATE → alterar
DELETE → apagar







 <img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/a152c53e-4a2e-4a17-8699-8c67ee53ae79" />



