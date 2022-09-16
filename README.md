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
  ```Java
  public static void teste () {
  }
  ```
  * Nomes válidos e boas práticas 
  * Parâmetros 
  * Retorno
  * Utilização de métodos estáticos 
    * Disponíveis na mesma classe
    * Disponíveis em outra classe/arquivo. 
  * Recursão 
* Classe
  * Definição
    É a estrutura de um objeto que possui e atributos e métodos;
    * Representação de classe e objeto na UML
    ![image](https://user-images.githubusercontent.com/73833452/190480070-15453aca-62fd-4772-a712-d7e4eaf587e5.png)

    * Diferença entre classe e objeto
      Classe é a estrutura e o objeto é o conteúdo estruturado pela classe;
    
  * Atributos
    São as propriedade da classe como: nome, idade e etc..
  * Métodos
    São as funções, as ações executadas pela classe.
  * Construtor
    É a primeira função executada pela classe que pode inicializar o objeto.
  * Objeto
    É o conteúdo estruturado de uma classe com dados;
  * Inicialização de um objeto
    ```Java
      pessoa pes = new Pessoa();
    ```
  * Utilização de um objeto
  ```Java
    pes.nome = "Henry";
  ```
  * Comparação de objetos
    ```Java
    pes1.equals(pes2); //retorna true ou false
    ```
  * Método toString
  * Visibilidade de atributos e métodos
    * Público
      ```Java
        public String nome;
      ```
    * Privado 
      ```Java
        private String nome;
      ```
  * Sobrecarga de métodos
       ```Java
        @Override
        public void teste(){
        }
      ```
  * Sobrecarga de construtores
  Uma classe java pode conter mais de um construtor podendo fazer com que o objeto possa ser criado de jeitos diferentes, como por exemplo com a passagem parametros ou sem.
* Pacotes 
  * Definição
    São utilizados para fazer a organização de classes.
     * Representação de pacotes na UML
     ![image](https://user-images.githubusercontent.com/73833452/190484446-318f11ee-c29c-4e8d-9e21-ee299ff606c2.png)

  * Definição de um pacote em uma classe
    São utilizados para fazer a organização de classes.
  * Importando uma classe de um pacote diferente
    É impossível importar classes para outro pacote
  * Visibilidade de classes, atributos e métodos
     * Default/Pacote  
  * Pacote default
      ```Java
      import package;
      ```
    * Importar uma classe em um pacote default 
      ```Java
      import package.pacote;
      ```
* Escopo de classe e objeto
  * Definição 
    O escopo de uma classe são os limites de até onde serta funcionalidade tem efeito sobre a aplicação.
  * Palavra reservada static
  * São métodos que não tem nenhuma dependencia de objetos e não dependem de nenhum conteúdo.
* Herança
  * Definição
    Permite que as classes java possuam uma estrutura onde podem ocorrer classes pais e filhas que podem herdar comportamentos.
     * Representação de herança na UML
     ![image](https://user-images.githubusercontent.com/73833452/190485747-9cdec90e-8ed6-46c7-88a1-9824192866ea.png)

  * Criação de uma classe que realiza herança 
  ```Java
  public class Pessoa {
    public String nome;
    public String cpf;
  }
  
  public class Aluno extends Pessoa {
    public Aluno(String nome, String cpf){
    super(nome, cpf)
    }
  }
  ```
  * Sobreescrita de métodos
    A sobrescrita é fazer um método igual a classe pai na classe filha onde a que vai ser executada pode ser selecionada.
  * Polimorfismo
   Em Java, a visibilidade padrão de classes, atributos e métodos está restrita a todos os membros que fazem parte de um mesmo pacote
    * Conversão de tipos
      ```Java
        int a = 32;
        String ata = new Character((char)a).toString();
      ```


  * Visibilidade de atributos e métodos
     Em Java, a visibilidade padrão de classes, atributos e métodos está restrita a todos os membros que fazem parte de um mesmo pacote 
     * Protegido
      ```Java
      proctected class(){
      }
      ```
  * Palavra reservada super
    A palavra reservada super é utilizada para fazer referencia a métodos ou atributos da super classe
     * Encadeamento de construtor
     ```Java
      public Fiat(String motor, String modelo, double preco){
        super(modelo, preco);
      }
     ```
     * Encadeamento de método
     ```Java
      super.metodo().
     ```
* Interface
  * Definição
     * Representação de interface na UML
     ![image](https://user-images.githubusercontent.com/73833452/190530281-948bd695-23ff-4dbb-96f0-5af198e6057a.png)

  * Criação de uma classe que implementa uma interface
  
  ```Java
    public interface interface {
      public String getNome();
    }
  
    public class Quadrado implements interface {
    @Override
    public String getNome(){
      return this.nome;
    }
    }
  ```
  
  * Sobreescrita de métodos
  ```Java
    double ReajusteTeste()
      {
          double Reajuste();
      }

  ```
  * Polimorfismo
    O polimorfismo representa situações em que um objeto pode se comportar de diferentes maneiras ao receber uma mensagem.
    * Conversão de tipos 
* Classe abstrada ---------------------------------
  * Definição
    É um tipo de classe especial que não pode ser instanciada, apenas herdada. 
     * Representação de classe abstrata na UML
     * ![image](https://user-images.githubusercontent.com/73833452/190500676-be5a80a6-aac4-42ce-89f5-c6484dd452d5.png)

  * Criação de uma classe que extende uma classe abstrata
   ```Java
       public class ContaPoupanca extends Conta {

      @Override
      public void imprimeExtrato() {
        System.out.println("### Extrato da Conta ###");

        SimpleDateFormat sdf = new SimpleDateFormat("dd/MM/aaaa HH:mm:ss");
        Date date = new Date();

        System.out.println("Saldo: "+this.getSaldo());
        System.out.println("Data: "+sdf.format(date));
    }

   ```
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
