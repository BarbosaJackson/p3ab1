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
#### Abstrata
  - Motivação: Ter um objeto que represente as informações em comum de todos os tipos de usuário.
  - Solução: Criar uma classe abstrata que contenha as informações.

### Endereco
  - Motivação: Unir as informações de endereço em um lugar só.
  - Solução: Criar um objeto que tem as informações do endereço de uma pessoa e, por composição,  objeto de pessoa pode ter esses dados.
#### Métodos
##### cadastraEndereco
  - Motivação: Evitar a duplicação de código para cadastrar um endereço
  - Solução: Adicionar na classe endereço um método que realize todo o precesso de cadastro de endereço e retorne um Objeto de endereço para quem o chamar utilizar.

### Técnico
  - Motivação: Ter uma representação de um técnico para salvar suas informações
  - Solução: Criar um objeto que salve essas informações
#### Métodos
##### cadTecnico
- Motivação: Evitar a duplicação de código para cadastrar um técnico
  - Solução: Adicionar na classe Tecnico um método que realize todo o precesso de cadastro de um técnico e retorne um Objeto de Tecnico para quem o chamar utilizar.

### Professor
  - Motivação: Ter uma representação de um professor para salvar suas informações
  - Solução: Criar um objeto que salve essas informações
#### Métodos
##### cadProf
- Motivação: Evitar a duplicação de código para cadastrar um professor
  - Solução: Adicionar na classe Prof um método que realize todo o precesso de cadastro de um professor e retorne um Objeto de Prof para quem o chamar utilizar.

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
#### Métodos
##### mudarEstado
  - Motivação: mudar o estado do projeto para acompanhar seu desenvolvimento
  - Solução: Criar um método que o faça
##### adicionarAtividade
  - Motivação: Permitir a criação de novas atividades
  - Solução: criar um método que receba  Atividade e crie uma nova
##### EditarProjeto
  - Motivação: permitir alterar as informaçoes do projeto
  - Solução: criar um método

### Atividade
  - Motivação: agrupar as informações necessárias para ter uma atividade
  - Solução: Criar um objeto com esses atributos
#### Métodos
##### EditarAtividade
  - Motivação: editar as informações de uma atividade
  - solução: criar um métod que o faça

### Sistema
  - Motivação: Agrupar os usuários e projetos e realizar as operações do projeto
  - Solução criar uma classe com duas listas, uma para os usuários e outra para os projetos, sendo a de usuários uma lista da classe pessoa para que, com a herança, todos os tipos de usuário possam ser salvos na mesma lista.
#### Métodos
##### ConsultaUsuarios
  - Motivação: realizar a consulta para um usuário exibindo todos as suas informações
  - Solução: criar um método que receba o identificador do usuário itere pela lista de usuários e, caso encontre aquele identificador, exiba as informações do usuário.
##### ConsultaProjeto
  - Motivação: realizar a consulta para um projeto exibindo todos as suas informações
  - Solução: criar um método que receba o identificador do projeto itere pela lista de projetos e, caso encontre aquele identificador, exiba as informações do projeto.
##### ConsultaAtividade
  - Motivação: realizar a consulta para uma atividade exibindo todos as suas informações
  - Solução: criar um método que receba o identificador do projeto e da atividade itere pela lista de projetos e, caso encontre aquele identificador, busque agora o identifgicador da atividade, caso encontre, exibir as informações da atividade
##### AdicionarUsuario
  - Motivação: Adicionar um usuário ao sistema
  - Solução: Criar um método que leia as informações do usuário a ser cadastrado e, com elas, adicione a lista de usuários do sistema
##### AdicionarProjeto
  - Motivação: criar novos projetos e adicionar eles ao sistema
  - Solução: criar um método que passando o RG do coordenador, cheque as informações e crie um novo projeto.