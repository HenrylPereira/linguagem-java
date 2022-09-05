# Linguagem de programação Java
Revisão sobre a linguagem Java

## Tópicos de Estudos

* [Tipos de Dados e operadores](03.md)
 * Tipos de Dados
  
    Tipos primitivos: boolean, byte, char, short, int, long, float e double;
Strings, Arrays Primitivos e Objetos.


  * Declarações de variáveis

    As declaração são feitas atraves do nome junção do tipo de dado com o nome da variável, podendo também já receber um valor.
  
  * Nomes válidos para variáveis e boas práticas 
 Os nomes de variáveis geralmente são feitos em lowerCamelCase que é o padrão camelCase com a primeira letra minuscula. Existem alguns padrões obrigatorios para as variáveis como: Deve conter apenas letras, _ (underline), $ ou os números de 0 a 9
    * Deve obrigatoriamente se iniciar por uma letra (preferencialmente), _ ou $
    * Deve iniciar com uma letra minúscula (boa prática – ver abaixo)
    * Não pode conter espaços
    * Não podemos usar palavras reservadas do sistema.

  * Atribuição de valores
  
    * São utilizados para difinir ou redefinir valores a variáveis.

  * Operadores
    * Operadores aritméticos
        * Operadores utilizados para realização de operações matemáticas primitivas. +, -, *, / e %
        
    * Operadores booleanos
        * Operadores utilizados para verificar se alguma condição é verdadeira ou falsa, como: &&, ||.
    
  * Conversão de tipos de dados
    * Existem várias conversões de dados possiveis em Java como por exemplo:
    ```Java
    double d = 10.0;
    String str = Double.toString(d);
    ```
  
* [Saída de Dados](04.md)
  * Método System.out.println
    ```Java
    System.out.println("Hello World");
    ```
  
  * Método System.out.print
      ```Java
    System.out.print("Hello World");
    ```
    
  * Exibir o valor de uma variável
  * 
    ```Java
    String s = "Hello World";
    System.out.print(s);
    ```
    
  * Exibir o valor de um decimal
    ```Java
    String d = 10.00;
    System.out.print(d);
    ```
* Classe Math
  * Definição
    * Java Math é uma classe que possibilita resolver operações matemáticas mais complexas.

  * Principais operações 
    * Math.max( x,y ), Math.min( x,y ), Math.sqrt( x ), Math.abs( x ), Math.random()
* String
  * Concatenação de String
  ```Java
     String s1 = "Olá ";
     String s2 = "Mundo!";
     System.out.println( s1.concat( s2 ) );
     System.out.println( s1 + s2 );
  ```
  * Principais operações sobre String
    * charAt, codePointAt, compareTo e compareToIgnoreCase, endsWith e startsWith, toCharArray, getBytes, isEmpty, split, substring e subSequence.
    ```Java 
    String valor = "Henry";
    System.out.println(valor.subSequence(0, 2));
    
    //Saída: Hen
    ```
  * Comparação de String
    ```Java
    String literal = "str";
    String outraLiteral = "str";

    System.out.println(literal == outraLiteral); //exibe true
    ```
  * Diferença entre String e caracter
    ```Java
    String str1 = "str";
    String str2 = "str";

    System.out.println(st1 == str2); 
    //exibe true
    ```
* Entrada de Dados
  * Classe Scanner
  É a classe que possibilita a entrada de valores pelo terminal.
  ```Java
    Scanner scan = new Scanner(System.in);
  ```
    * Obter um valor inteiro
    ```Java
     Int i = scan.nextInt();
    ```
    * Obter um valor decimal
    ```Java
     Double d = scan.nextDouble();
    ```
    * Obter um valor de texto 
    ```Java
     String s = scan.nextLine();
    ```
* Fluxo de Controle
  * Estruturas de Decisões
    * if-else-then
      ```Java
        if (condição 1) {
            // se a consição 1 for verdadeira
        } else if (condição 2) {
            // se a consição 1 for falsa e a condição 2 for verdadeira
        } else {
            // se as condições anteriores não forem verdadeiras
        }
      ```
      ```Java
        b = (a > 0) ? 1 : 2; //IF ternário
      ```
    * switch
      ```Java
        switch (condição) {
        case valor1:
        // se valor1
        break;
        case valor2:
        // se valor2
        break;
      ```

  * Estruturas de Repetições
    * for
      ```Java
        for (inicialização da variável; checagem de condição; incremento/decremento do valor da variável) {  
            comando a ser executado/declaração
        }
      ```
    * while
       ```Java
        while(condição)  {
            enquanto a condição for verdadeira
        }
      ```
    * do-while 
    ```Java
      do {
           // enquanto codição for verdadeira
      } while (condição);
    ```
    * Comandos break e continue
     ```Java
      for (int i = 0; i < 10; i++) {
        if (i == 4) {
          continue;
        }
        if (i == 5) {
          break;
        }
        System.out.println(i);
      }
    ```
* Arranjos e Matrizes
  * Definição matemática
   * Difinição matemárica de arranjo: "Agrupamentos formados com p elementos de um conjunto de n elementos"
   * Difinição matemárica de matriz: "Matriz é uma tabela organizada em linhas e colunas no formato m x n"
  * Declaração de arranjos
     ```Java
        String[] carros = {"Volvo", "VW", "Ford", "Fiat"};
    ```
  * Declaração de matrizes
   ```Java
      int[][] tab = new int[2][2];
    ```
  * Percorrer arranjos
   ```Java
      String[] carros = {"Volvo", "VW", "Ford", "Fiat"};
      for(String carro : carros){
        //para cara carro
      }
    ```
  * Percorrer matrizes
   ```Java
      int[][] tab = new int[10][9];
      for(int i = 0; i < 10; i++)
        for(int j = 0; j < 9; j++) tab[i][j] = i*j; 
    ```
    * Linha a linha
   ```Java
      int[][] tab = new int[10][9];
      for(int i = 0; i < 10; i++)
    ```
    * Coluna a coluna
   ```Java
      int[][] tab = new int[10][9];
      for(int i = 0; i < 10; i++)
        for(int j = 0; j < 9; j++) tab[i][j] = i*j; 
    ```
    * Em diagonal 
    ```Java
        for(i=M-1; i>=0; i--){
          for(j=N-1; j>=0; j--){
    ```

  * Utilizar arranjos e matrizes como parâmetros de métodos 
  * Utilizar arranjos e matrizes como retorno de métodos 
* Tratamento de Exceções
  
  * Definição
  O tratamento de exceções é feito para tratar casos inesperados no código.
  * Exceções comuns
    * Divisão por zero
      ArithmeticException: / by zero;
    * Conversão de tipos de dados inválidos
    * Acessar uma posição inválida em um arranjo
      ArrayIndexOutOfBoundsException;
    * Acessar uma String nula
  * Bloco para capturar uma exceção 
    ```Java
    try {
    //código a ser exec
    } catch (Exception e) {
    //executa caso der erro;
    } finally {
    //executa de qualquer forma no final;
    }
    ```
  
* Métodos estáticos
  * Estrutura de declaração de um método estático
  * Nomes válidos e boas práticas 
  * Parâmetros 
  * Retorno
  * Utilização de métodos estáticos 
    * Disponíveis na mesma classe
    * Disponíveis em outra classe/arquivo. 
  * Recursão 
* Classe
  * Definição
    * Representação de classe e objeto na UML
    * Diferença entre classe e objeto
  * Atributos
  * Métodos
  * Construtor 
  * Objeto
  * Inicialização de um objeto 
  * Utilização de um objeto
  * Comparação de objetos
  * Método toString
  * Visibilidade de atributos e métodos
    * Público
    * Privado 
  * Sobrecarga de métodos
  * Sobrecarga de construtores
* Pacotes 
  * Definição
     * Representação de pacotes na UML
  * Definição de um pacote em uma classe
  * Importando uma classe de um pacote diferente
  * Visibilidade de classes, atributos e métodos
     * Default/Pacote  
  * Pacote default
    * Importar uma classe em um pacote default 
* Escopo de classe e objeto
  * Definição 
  * Palavra reservada static 
* Herança
  * Definição
     * Representação de herança na UML
  * Criação de uma classe que realiza herança 
  * Sobreescrita de métodos
  * Polimorfismo
    * Conversão de tipos 
  * Visibilidade de atributos e métodos
     * Protegido
  * Palavra reservada super 
     * Encadeamento de construtor 
     * Encadeamento de método
* Interface
  * Definição
     * Representação de interface na UML
  * Criação de uma classe que implementa uma interface
  * Sobreescrita de métodos
  * Polimorfismo
    * Conversão de tipos 
* Classe abstrada
  * Definição
     * Representação de classe abstrata na UML
  * Criação de uma classe que extende uma classe abstrata
  * Polimorfismo
    * Conversão de tipos 
* Coleções 
  * Definição
  * List e Arraylist 
    * Aplicações
    * Declaração
    * Utilização
      * Adicionar elementos
      * Acessar elementos
      * Atualizar elementos 
      * Remover elementos 
  * Map e HashMap
    * Aplicações 
    * Declaração
    * Utilização
      * Adicionar elementos
      * Acessar elementos
      * Atualizar elementos 
      * Remover elementos 
* Tipo Enumerado
  *  Definição
     * Representação de tipos enumerados na UML
* Representação de tempo
  * Classe Date
  * Classe Calendar
  * API Date/Time Java 8
    * LocalDate
    * LocalTime
    * LocalDateTime
    * Period
    * Duration
    * Formação de Date/Time 
* Modificador final
  * Definição
    * Representação de final no diagrama UML 
  * Modificador final em uma variável
    * Variável  de tipo primitivo
    * Objeto 
  * Modificador final em um atributo
    * Atributo primitivo
    * Objeto 
  * Modificador final em um método
  * Modificador final em uma classe
* Objeto imutável
  * Definição
  * Aplicações
  * Como criar um objeto imutável
  * Como modificar um objeto imutável 
* Tipos Genéricos
  * Definição
     * Representação de tipos genéricos na UML
  * Criação de classes com tipos genéricos
  * Inicialização de objetos com tipos genéricos  
* Testes Unitários
  * TDD
  * JUnit
    * Adicionar JUnit no projeto Java
  * Teste assertEquals
  * Teste assertTrue/assertFalse
  * Teste assertNull/assertNull
  * Teste assertArrayEquals  
  * Teste fail
  * Teste capturar uma exception
* JDBC
  * Definição
  * Driver de conexão 
  * Como adicionar o driver de conexão no projeto Java
  * Criação de uma conexão com o banco de dados
    * Classe DataManager
    * String de conexão
      * Banco SQLite
      * Banco MySql
      * Banco Postgre 
    * Classe Connection
  * Enviar instruções SQL
    * Classe Statement
    * Classe PreparedStatment   
  * Consultar registros no banco de dados
    * Classe ResultSet
    * Obter um registro
    * Obter uma coleção de registros
  * Bloco de instruções try-with-resources
  * Captura de exceções
    * Driver não encontrado
    * Conexão inválida
    * Tabela não encontrada
    * Registro não encontrado
    * Erro ao inserir/atualizar
    * Erro ao consultar
  * Design Patterns
    * Singleton Factory para criação de conexões   
      * Representação na UML
    * DAO para manipular dados de uma tabela   
      * Representação na UML

## Listas de Exercícios

[SCHEIBEL, Glaucio. Exercícios de Programação](https://github.com/glaucioscheibel/exercicios)

[Beecrowd](https://www.beecrowd.com.br/judge/pt/)

[Leetcode](https://leetcode.com)

[HackerRank](https://www.hackerrank.com)

[Exercism](https://exercism.org/tracks/java)



## Referências Bibliográficas

FURGERI, SÉRGIO. Java 8 Ensino Didático: Desenvolvimento e Implementação de Aplicações. Saraiva Educação SA, 2018.

Schildt, Herbert. Java para iniciantes. Bookman Editora, 2015.

Finegan, Edward, and Robert Liguori. OCA Java SE 8: Guia de Estudos para o Exame 1Z0-808. Bookman Editora, 2018.

Bloch, Joshua. Java Efetivo: 3a edição. Alta Books Editora, 2019.

Martin, Robert C. Código limpo: habilidades práticas do Agile software. Alta Books, 2019.

Fowler, Martin. UML Essencial: um breve guia para linguagem padrão. Bookman editora, 2014.
