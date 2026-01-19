# COMECE POR AQUI
#PRÉ-REQUISITOS
- Java JDK 21 ou superior
- Eclipse IDE (recomendado) ou qualquer IDE Java

## COMO EXECUTAR
No Eclipse IDE

Importe o projeto:

File → Import → Existing Projects into Workspace
Selecione a pasta do projeto
Execute o sistema:

Navegue até: src/biblioteca/Sistema.java
Clique direito → Run As → Java Application

## Funcionalidades
1. **Cadastro de Itens**: Livros e Revistas
2. **Cadastro de Usuários**: Alunos e Funcionários
3. **Empréstimos**: Realizar empréstimos de itens para usuários
4. **Devoluções**: Registrar a devolução de itens
5. **Relatórios**: Listar itens, usuários, empréstimos ativos e estatísticas
6. **Demonstração de Polimorfismo**: Mostrar o uso de polimorfismo com os dados cadastrados

## Conceitos de POO Aplicados

### 1. Encapsulamento
- Atributos privados com métodos públicos de acesso (getters)
- Controle de acesso aos dados internos das classes

### 2. Herança
- `Aluno` e `Funcionario` herdam de `Usuario`
- `MostrarLivro` e `MostrarRevista` herdam de `Item`

### 3. Polimorfismo
- Método `obterInformacoes()` em `Item` é sobrescrito nas subclasses
- Método `getTipoUsuario()` em `Usuario` é sobrescrito nas subclasses
- Uso de arrays de tipos base (`Item[]`, `Usuario[]`) para processar objetos de tipos diferentes

### 4. Classes Abstratas
- `Item` é classe abstrata com método abstrato `obterInformacoes()`
- `Usuario` é classe abstrata com método abstrato `getTipoUsuario()`

### 5. Interface
- `RelatorioBiblioteca` com método `gerarRelatorio()` (exemplo de interface)

### 6. Associações
- `SistemaBiblioteca` tem associações 1:N com `Item`, `Usuario` e `Emprestimo`
- `Emprestimo` tem associações 1:1 com `Usuario` e `Item`

### 7. Atributos e Métodos Estáticos
- `totalFuncionarios` e `getTotalFuncionarios()` em `Funcionario`
- `totalOperacoes` e `getTotalOperacoes()` em `SistemaBiblioteca`

#ESTRUTURA
BibliotecaPOO/

├── src/biblioteca/
│   ├── Aluno.java                    # Herda de Usuario
│   ├── Biblioteca.java               # Representa a biblioteca física
│   ├── Emprestimo.java               # Representa um empréstimo individual
│   ├── Funcionario.java              # Herda de Usuario (com atributo estático)
│   ├── Item.java                     # Classe abstrata para itens
│   ├── MostrarLivro.java             # Herda de Item (Livro físico)
│   ├── MostrarRevista.java           # Herda de Item (Revista)
│   ├── RelatorioBiblioteca.java      # Interface para relatórios
│   ├── Sistema.java                  # Classe principal com menu
│   ├── SistemaBiblioteca.java        # Gerencia operações (com atributo estático)
│   └── Usuario.java                  # Classe abstrata base para usuários
├── DiagramaClasses.png               # Diagrama UML do sistema
└── README.md                         # Este arquivo
  
## Autores
- Fátima Letícia - Thainara Miranda - Werlon Afonso
