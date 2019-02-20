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

## Clases

### Pessoa
  - Motivação: Diminuir a repetição de código encontrada em usuários do sistema (como as informações de nome e endereço por exemplo).
  - Solução: Criar uma classe abstrata contendo as informações repetidas e fazer as classes que são tipos de pessoa no sistema herdarem essas informações da classe pessoa.
  - Vantagens: Evita a duplicação de código.

### Endereco
  - Motivação: Unir as informações de endereço em um lugar só
  - Solução: Criar um objeto que tem as informações do endereço de uma pessoa e, por composição,  objeto de pessoa pode ter esses dados

### Técnico
  - Motivação: Ter uma representação de um técnico para salvar suas informações
  - Solução: Criar um objeto que salve essas informações

### Professor
  - Motivação: Ter uma representação de um professor para salvar suas informações
  - Solução: Criar um objeto que salve essas informações

### Pesquisador
  - Motivação: Ter uma representação de um pesquisador para salvar suas informações
  - Solução: Criar um objeto que salve essas informações

### Aluno
  - Motivação: Ter uma representação de um aluno para salvar suas informações
  - Solução: Criar um objeto que salve essas informações

### Profissional
  - Motivação: Ter uma representação de um profissional para salvar suas informações
  - Solução: Criar um objeto que salve essas informações

### Coordenador
  - Motivação: ter as informações dos projetos em um lugar, entrando nos Objetos que tem a permissão de um coordenador como um atributo de composição
  - Solução: Criar um objeto com os projetos e as informações de um coordenador

### Periodo
  - Motivação: Salvar a data e hora em um só lugar
  - Solução:Criar um objeto com os atributos sendo data e hora

### Projeto
  - Motivação: agrupar as informações necessárias para ter um projeto
  - Solução: Criar um objeto com esses atributos

### Atividade
  - Motivação: agrupar as informações necessárias para ter uma atividade
  - Solução: Criar um objeto com esses atributos

### Sistema
  - Motivação: Agrupar os usuários e projetos e realizar as operações do projeto
  - Solução criar uma classe com duas listas, uma para os usuários e outra para os projetos, sendo a de usuários uma lista da classe pessoa para que, com a herança, todos os tipos de usuário possam ser salvos na mesma lista.
