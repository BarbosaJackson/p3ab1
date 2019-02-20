# Sistema de produtividade academica

## Funcionalidades

### Adicição e remoção de informações aos projetos  e atividades
Nas respectivas classes existe um método **editar** que permite fazer isso.

### Associação de usuários
Na classe **Projeto** existe o método **adiocionarUsuario** que recebe o identificador do profissional e o adiciona no projeto.

### Alterar o status do projeto

Na classe projeto existe o método **mudarEstado** que muda o projeto para o próximo estágio fazendo as verificações necessárias para isso.

### Consultas
Na classe que contém as atividades básicas do sistema existem três métodos cada um para um tipo de consulta, no caso por usuário, projto e atividade.

### Gerar relatório
Na classe **Sistema** existe um método que para tal, é passado um inteiro com o tipo de relatório, os tipos são:
  1. lista de usuários no sistema e em quais projetos eles estão associados
  2. lista de projetos cadastrados no sistema
  3. lista de atividades cadastradas no sistema

