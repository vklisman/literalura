# Literalura

Literalura é uma aplicação Java com Spring Boot que permite buscar livros, listar livros registrados, listar autores, e muitas outras funcionalidades, baseada na API Guntendex.

## Tecnologias Utilizadas

- **Java 17**
- **Spring Boot**
- **Hibernate**
- **PostgreSQL**
- **Gutendex API**
- **Maven**

## Funcionalidades

1. **Buscar livros pelo título**: Consulta a API Gutendex para buscar livros pelo título.
2. **Listar livros registrados**: Exibe todos os livros registrados no banco de dados.
3. **Listar autores registrados**: Exibe todos os autores dos livros registrados.
4. **Listar autores vivos em um determinado ano**: Lista autores que estavam vivos em um ano especificado.
5. **Listar autores nascidos em determinado ano**: Lista autores que nasceram em um ano especificado.
6. **Listar autores por ano de sua morte**: Lista autores que morreram em um ano especificado.
7. **Listar livros em um determinado idioma**: Lista livros registrados no banco de dados em um idioma especificado.
8. **Encerrar a aplicação**: Encerra o programa.

## Configuração do Projeto

### Pré-requisitos

- Java 17 ou superior
- Maven
- PostgreSQL

## Estrutura do Projeto

- `br.com.alura.literalura`: Pacote principal do projeto.
   - `principal`: Contém a classe `Principal`, que gerencia a execução da aplicação.
   - `model`: Contém as classes de modelo (`Livro`, `Autor`, `LivroDTO`, `AutorDTO`).
   - `repository`: Contém as interfaces de repositório Spring Data JPA.
   - `service`: Contém as classes de serviço (`ConsumoAPI`, `ConverteDados`).

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/literalura.git
   cd literalura
   ```

2. Configure o banco de dados no arquivo `application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/literalura
   spring.datasource.username=seu-usuario
   spring.datasource.password=sua-senha
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   ```

3. Execute o projeto:
   ```bash
   mvn spring-boot:run
   ```


## Uso

Ao iniciar a aplicação, o menu principal será exibido com as opções disponíveis. Basta seguir as instruções na tela para navegar pelas funcionalidades.

### Exemplo de Uso

1. **Buscar livros pelo título**:
   - Digite `1` e pressione Enter.
   - Insira o título do livro que deseja buscar.
   - A aplicação fará uma consulta à API Gutendex e exibirá os resultados encontrados.

2. **Listar livros registrados**:
   - Digite `2` e pressione Enter.
   - A aplicação listará todos os livros registrados no banco de dados.

3. **Listar autores registrados**:
   - Digite `3` e pressione Enter.
   - A aplicação listará todos os autores dos livros registrados.

4. **Listar autores vivos em um determinado ano**:
   - Digite `4` e pressione Enter.
   - Insira o ano desejado.
   - A aplicação listará os autores que estavam vivos naquele ano.

5. **Encerrar a aplicação**:
   - Digite `0` e pressione Enter.
   - A aplicação será encerrada.
