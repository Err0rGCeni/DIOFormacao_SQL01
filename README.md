# Fundamentos de Banco de Dados

## Introdução a Banco de Dados

- Definições;
- Fases;
- Sistemas de Gerenciamento de Banco de Dados;
- Mercado;

## Sistemas de Gerenciamento de Banco de Dados

- Abordagens;
- Isolamento e Abstração;
- Views;
- Compartilhamento e Transações;
- Atores;

## Modelagem de Dados para Banco de Dados

- Modelagem;
- SQL básico (MySQL);

## Revisão: Bancos de Dados

- **Dados**: fatos conhecidos que podem ser reistrados e possuem significado implícito.
- **Banco de Dados**: coleção de dados relacionados.
  - Representa algum aspecto do mundo real (mini-mundo/universo de discurso);
  - Coleção logicamente coerente de dados com algum significado inerente;
  - É projetado, construído e populado com dados para uma finalidade específica, para um grupo específico de usuários;
- **SGBD**: sistema gerenciador de banco de dados, coleção de programas que permite aos usuários criar e manter um banco de dados.
  - Definição: especificar os tipos, estruturas e restrições dos dados armazenados;
  - Construção: processo de armazenar os dados em algum meio controlado pelo SGBD;
  - Manipulação: funções como consulta, atualização, geração de relatórios;
  - Compartilhamento: permitir que diversos usuários acessem-no simultaneamente;
  - Proteção: proteger o sistema contra defeitos/falhas de hardware e software, e proteger a segurança contra acessos indesejados;
- **Sistema de Banco de Dados**: união do banco de dados com o software de SGBD.
  - Softwares SGBD: processamento de consultas/programas, e acesso aos dados;
  - Sistema de Banco de Dados: programas de aplicação, softwares sgbd, dados e metadados;
- **Catálogo de banco de dados** (Natureza autodescritiva): definição completa da estrutura (estrutura de cada arquivo, tipo, formato de armazenamento de cada item de dados) e restrições de um sistema de banco de dados.
- **Independência entre Dados e Programas**: permite que a estrutura dos arquivos de dados seja armazenada sepradamento do código dos programas de acesso
  - Alterações na estrutura do banco de dados não afetam diretamento as aplicações externas.
- **Visão do Usuário** (view): subconjunto do banco de dados, representação personalizada dos dados.
  - Permite que usuários vejam apena as informações relevantes para suas necessidades.
- **DBA** (DataBase Admin): administrador do banco de dados.
  - Autorização de acesso ao banco de dados;
  - Coordenar e monitorar a utilização;
  - Adquirir recursos de software e hardware conforme a nacessidade;
  - Manegamento de problemas com falhas na segurança e demora no tempo de resposta do sistema;  
- **Usuário final**: pessoa cujas funções exigem acesso ao banco de dados para consultas, atualizações e geração de relatórios.
  - Casuais, Naives, Sofisticados, Isolados;
- **Transação Programada**: tipos padrão de consultas e atualizações do banco de dados, que foram cuidadosamente programadas e testadas.
- **Sistema de Banco de Dados Dedutivo**: sistemas que oferecem capacidades para definir regras de dedução/inferência para novas informações com base nos fatos armazenados.
- **Objeto Persistente**: objetos que continuam existindo mesmo após o encerramento do programa/aplicação que os criou.
- **Metadados**: Definição do banco de dados armazenado.
  - Descrição/Esquema;
  - Construtores;
  - Constrains;
- **Aplicação para Processamento de Transação**: sistemas de reserva ou bancos de dados bancários.

## Revisão: Conceitos e Arquiteturas

- **Modelo de dados**: Coleção de conceitos que podem ser usados para descrever a estrutura de um banco de dados.
- **Esquema de banco de dados**: Descrição do banco de dados, especificado durante o projeto.
- **Estado de banco de dados**: Dados no banco de dados em determinado momento no tempo
- **Esquema interno**: Descrição da estrutura do armazenamento físico do banco de dados. Descreve os detalhes completos do armazenamento de dados e caminhos de acesso para o banco de dados.
- **Esquema conceitual**: Descreve a estrutura do banco de dados inteiro para uma comunidade de usuários. Oculta detalhes das estruturas de armazenamento físico, concentrando na descrição de entidades, tipos de dados, relacionamentos, operações de usuários e restrições.
- **Esquema externo**: Descreve uma parte do banco de dados para um grupo de usuários específicos.
- **Independência de dados**: Capacidade de alterar o esquema em um nível do sistema de banco de dados sem alterar o esquema no nível mais alto.
  - Lógica: Capacidade de alterar o esquema conceitual sem ter de alterar os esquemas externos ou os programas de aplicação;
  - Física: Capacidade de alterar o esquema interno sem ter de alterar o esquema conceitual
- **DDL** (Data Definition Language): linguagem utilizada para definir a estrutura ou esquema do banco de dados. Ela permite que os usuários criem, modifiquem e excluam objetos no banco de dados.
- **DML** (Data Manipulation Language): linguagem que o SGBD oferece com um conjunto de operações para finalidades de manipulação dos dados.
- **SDL** (Storage Definition Language): linguagem, menos comum, específica para cada sistema de gerenciamento de banco de dados. Ele lida com detalhes relacionados ao armazenamento físico dos dados.
- **VDL** (View Definition Language): linguagem utilizada para definir visões (views).
