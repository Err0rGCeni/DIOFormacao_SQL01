# Modelagem de Dados para Banco de Dados

> Modelagem: Possui foco na descrição e relacionamento dos elementos que compões a representação do contexto (mini-mundo)

Pode-se subdividir em Representação, Modelo e Referência.

- Mini-mundo: delimitando o contexo dos dados;
- Alto nível: requisitos para a criação do modelo;
- Esquema: definindo estrutura relacional;
- SGBD: implementado e criando o DB;

## Comandos Básicos SQL

Utilizando o MySQL CLI no Windows

```sql
-- Mostra a lista de bancos de dados existentes
SHOW DATABASES;
```

```sql
-- Cria um novo banco de dados chamado "RegistroDePubli"
CREATE DATABASE RegistroDePubli;
```

```sql
-- Seleciona o banco de dados "RegistroDePubli" para uso
USE RegistroDePubli;
```

```sql
-- Apaga o banco de dados "RegistroDePubli"
DROP DATABASE RegistroDePubli;
```

```sql
-- Cria um novo banco de dados chamado "FirstEx", o seleciona e define duas tabelas: "periodicos" e "editora"
CREATE DATABASE FirstEx;
USE FirstEx;
CREATE TABLE periodicos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome_periodico VARCHAR(20),
    issn INT UNIQUE,
    id_editora INT
);
CREATE TABLE editora (
    id INT AUTO_INCREMENT,
    nome_editora VARCHAR(120) UNIQUE,
    pais VARCHAR(5),
    PRIMARY KEY(id)
);
```

```sql
-- Adiciona uma restrição de chave estrangeira à tabela "periodicos" referenciando a tabela "editora"
ALTER TABLE periodicos ADD CONSTRAINT fk_editora_periodico FOREIGN KEY (id_editora) REFERENCES editora(id);
```

```sql
-- Insere dados na tabela "editora"
INSERT INTO editora (nome_editora, pais) VALUES ('IEEE', 'EUA'), ('DataScienceMagazine', 'EUA');
INSERT INTO editora (nome_editora, pais) VALUES ('IEEE', 'EU');
INSERT INTO editora (nome_editora, pais) VALUES ('IEEE_EU', 'EU');
```

```sql
-- Insere dados na tabela "periodicos"
INSERT INTO periodicos (nome_periodico, issn, id_editora) VALUES ('Special Issue', '156795164', '1');
INSERT INTO periodicos (nome_periodico, issn, id_editora) VALUES ('Special Issue 2', '136955764', '1');
INSERT INTO periodicos (nome_periodico, issn, id_editora) VALUES ('Prob', '236955768', '2');
```

```sql
-- Seleciona dados das tabelas "peiodicos" e "editora"
SELECT * FROM periodicos;
SELECT * FROM editora;
```
