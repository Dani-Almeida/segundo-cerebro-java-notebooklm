# Especialista em Java com NotebookLM

Projeto do desafio da DIO sobre a criação de um segundo cérebro com IA. Usei o NotebookLM como mentor de estudos para revisar Java, praticar explicações com minhas próprias palavras e me preparar para entrevistas de estágio e júnior.

## Tema e objetivo

Comecei pelos fundamentos da linguagem e da plataforma Java. Meu objetivo é conseguir explicar como cada conceito funciona, quando ele se aplica e por que eu o usaria. Para praticar, combino aulas, exemplos de código, simulações de entrevista e flashcards.

## Fontes escolhidas

| Fonte | Formato | Por que escolhi |
| --- | --- | --- |
| [Java Básico — Loiane Groner](https://www.youtube.com/playlist?list=PLGxZ4Rq3BOBq0KXHsp5J3PxyFaBIXVs3r) | Aulas em vídeo | Apresenta sintaxe, orientação a objetos e exceções em português, com exercícios. |
| [Java Intermediário — Loiane Groner](https://www.youtube.com/watch?v=EdEKx24xHGc&list=PLGxZ4Rq3BOBoqYyFWOV_YbfBW80YGAGEI) | Aulas em vídeo | Dá continuidade ao curso básico com assuntos como enums e classes wrapper. |

Escolhi Loiane Groner porque ela reúne experiência profissional em desenvolvimento, reconhecimento como Java Champion e material gratuito em português que consigo acompanhar e praticar. [Perfil de Loiane Groner na Oracle](https://apexapps.oracle.com/pls/apex/r/ace_program/oracle-aces/ace?ace_id=672&clear=2).

### Referências recomendadas pelo NotebookLM

| Referência | Como pretendo usar |
| --- | --- |
| [Dev.java](https://dev.java/) | Consultar tutoriais de sintaxe, coleções, lambdas e Streams. |
| [Inside Java](https://inside.java/) | Acompanhar novidades e consultar episódios sobre recursos mais avançados da plataforma. |
| [Java Design Patterns](https://github.com/iluwatar/java-design-patterns) | Ler implementações em Java quando chegar ao estudo de padrões de projeto. |
| [Manning](https://www.manning.com/catalog) e [O’Reilly](https://www.oreilly.com/) | Buscar livros de apoio conforme o tema em estudo. |

A pesquisa do NotebookLM também sugeriu listas de cursos no Class Central e discussões no Reddit. Essas indicações ajudam a descobrir materiais. Para conferir detalhes técnicos e diferenças entre versões, a documentação oficial serve como referência.

### Livros reunidos para consulta

| Tema | Títulos da seleção |
| --- | --- |
| Linguagem Java | *Java Language Features* e *From Java 21 to Java 25*. |
| Estruturas de dados e algoritmos | *Beginning Java Data Structures and Algorithms*, *Data Structures and Algorithms in Java*, *Fabulous Adventures in Data Structures and Algorithms* (prévia) e *40 Algorithms Every Programmer Should Know*. |
| Testes | *Pragmatic Unit Testing in Java with JUnit*. |
| Spring Boot e APIs | *Beginning Spring Boot 3* e *Spring Boot 3 API Mastery*. |
| Banco de dados | *Database Design and Modeling with PostgreSQL and MySQL* e *Mastering PostgreSQL*. |
| Concorrência | *Modern Concurrency in Java* e *Virtual Threads, Structured Concurrency, and Scoped Values*. |
| Arquitetura e DDD | *Designing Hexagonal Architecture with Java*, *Learning Domain-Driven Design*, *Mastering Domain-Driven Design*, *Implementing Domain-Driven Design* e *Patterns, Principles, and Practices of Domain-Driven Design*. |
| Microsserviços e sistemas distribuídos | *Microservices with Spring Boot and Spring Cloud*, *Quarkus in Action*, *Kubernetes Native Microservices with Quarkus*, *Think Distributed Systems* e *System Design Interview*, volume 2. |
| Preparação para entrevistas | *Guide To Clear Java Developer Interview*. |

## Diretriz do notebook

Configurei o NotebookLM para atuar como mentor técnico em Java. Ele começou perguntando meu nível, quais assuntos eu queria priorizar e se havia uma entrevista marcada. Informei que meu nível era básico e escolhi começar pelo primeiro módulo do plano sugerido.

- Usar linguagem simples e explicar por que e quando cada conceito se aplica.
- Trazer exemplos de código e analogias quando ajudarem a entender o conteúdo.
- Na simulação de entrevista, fazer uma pergunta por vez, aguardar minha resposta e apontar o que estava certo e o que precisava melhorar.
- Criar flashcards com uma pergunta, uma resposta curta e uma analogia quando ela ajudar na revisão.
- Indicar diferenças entre as versões do Java quando forem relevantes.

## Plano de estudo

| Módulo | Conteúdo | Situação |
| --- | --- | --- |
| 1. Plataforma e sintaxe | JDK, JRE, JVM, bytecode, JIT, tipos primitivos, wrappers, controle de fluxo e arrays | Iniciado com o tema de compilação e execução |
| 2. Orientação a objetos | Classes, objetos, construtores, encapsulamento, abstração, herança, polimorfismo, interfaces e classes abstratas | Planejado |
| 3. Coleções | `List`, `Set`, `Map`, `ArrayList`, `LinkedList`, `HashMap`, `equals()` e `hashCode()` | Planejado |
| 4. Exceções | Exceções verificadas e não verificadas, `try/catch/finally` e `try-with-resources` | Planejado |

## Perguntas, respostas e citações

### 1. Como um programa Java é executado?

Pedi para começar pelo módulo 1. O NotebookLM explicou que o compilador `javac` transforma o código-fonte `.java` em arquivos `.class` que contêm bytecode. Em seguida, apresentou o papel da JVM, do JDK, do ambiente de execução e do compilador JIT.

### 2. Um arquivo compilado no Windows executa no Linux?

O NotebookLM perguntou se eu poderia compilar um código no Windows e executar o arquivo `.class` em um servidor Linux sem recompilar.

> se tiver a JVM instalada na máquina do linux pode rodar o mesmo arquivo, pq a JVM lê o arquivo e vc consegue rodar no linux

O feedback destacou que eu identifiquei o papel da JVM e sugeriu nomear o bytecode e relacionar a resposta à ideia de *Write Once, Run Anywhere*.

**Minha resposta revisada**

> Sim. O arquivo `.class` contém bytecode que pode ser executado no Linux sem recompilar, desde que a JVM seja compatível com a versão desse bytecode e o programa tenha as dependências necessárias. Se o programa depender de bibliotecas nativas ou recursos específicos do Windows, essa dependência também precisa ser tratada.

**O que conferi na documentação**  
A especificação da JVM descreve o formato `.class` como independente de hardware e sistema operacional e registra quais versões do formato cada versão da plataforma aceita. Na execução, uma JVM pode interpretar bytecode e usar compilação JIT para converter trechos em código de máquina. [Especificação do formato `.class` — Oracle](https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-4.html) · [Manual do `javac` — Oracle](https://docs.oracle.com/en/java/javase/21/docs/specs/man/javac.html).

A transcrição do NotebookLM contém citações numeradas, como `[1]` e `[2]`. Os títulos e trechos correspondentes ainda precisam ser conferidos no próprio notebook.

## Materiais gerados

### Flashcard sobre JVM e bytecode

Pedi ao NotebookLM um flashcard depois da simulação de entrevista. Esta é a versão revisada para estudo.

**Pergunta**  
O que é JVM e qual é o papel do bytecode?

**Resposta**  
O `javac` compila o código-fonte em bytecode, armazenado em arquivos `.class`. Uma JVM compatível executa esse bytecode. Isso permite usar o mesmo arquivo em diferentes sistemas quando as dependências da aplicação também são compatíveis.

**Analogia**  
O bytecode é como uma receita escrita em símbolos que chefs de cozinhas diferentes conseguem seguir. Cada JVM é o chef que executa a receita com os recursos disponíveis em sua cozinha.

### Evidências da sessão

O registro da conversa inclui a definição do meu nível, o plano sugerido, a explicação inicial, a simulação de entrevista e o pedido de flashcard. O print recebido mostra o início da conversa, quando informei que meu nível era básico.

## Notebook compartilhado

O link de acesso ao notebook e os links para os prints ficam pendentes até que estejam disponíveis para inclusão no repositório.
