# Biblioteca SQLite

Este projeto implementa um sistema de gerenciamento de uma biblioteca utilizando SQLite. Ele permite o cadastro de autores, livros e registro de empréstimos.

## Estrutura do Banco de Dados

O banco de dados `biblioteca.db` possui as seguintes tabelas:

- **Autores**
  - `AutorID`: Identificador único do autor (chave primária).
  - `Nome`: Nome do autor.
  - `Nacionalidade`: Nacionalidade do autor.

- **Livros**
  - `LivroID`: Identificador único do livro (chave primária).
  - `Titulo`: Título do livro.
  - `AutorID`: Referência ao autor (chave estrangeira).
  - `AnoPublicacao`: Ano de publicação do livro.
  - `Genero`: Gênero do livro.

- **Empréstimos**
  - `EmprestimoID`: Identificador único do empréstimo (chave primária).
  - `LivroID`: Referência ao livro emprestado (chave estrangeira).
  - `DataEmprestimo`: Data em que o livro foi emprestado.
  - `DataDevolucao`: Data em que o livro foi devolvido (pode ser nulo se ainda não devolvido).
  - `NomeUsuario`: Nome do usuário que fez o empréstimo.

## Como Usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/biblioteca-sqlite.git
   cd biblioteca-sqlite
