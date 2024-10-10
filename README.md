                                                  LABORATÓRIO DE PROGRAMAÇÃO II 

-----------------

### **Aula 2 - Algoritmos Lineares**

* Diferença entre Eficácia e Eficiência:

        Eficácia - Conceito digital - 0 ou 1 / algoritmo resolve ou não o problema
        
        Eficiência - Conceito analógico - O quão bem (eficientemente) o algoritmo resolve o peoblema da melhor maneira => 0% - 100%

* Qdo começar a programar, primeiro pensar na eficácia e depois na eficiência

* Recursividade - É a capacidade do algoritmo de reexecutar a si mesmo

* Programação Algoritmo: Entrada -> Processamento -> Saída

* Entrada de dados:

        int() números  
        float() - números com decimais  
        string() - Textos  
        boolean() - False or True / 0 or 1   
        
        idade = int(input(‘Digite sua idade: ‘))  
        salario = float(input(‘Digite seu salário: ‘))  
        Nome = str(input(‘Digite o seu nome: ‘))  
        pcd = bool(input(‘Pessoa com deficiência: ‘))  

-----------------

### **Aula 3 - Estruturas Condicionais**

* A estrutura condicional simples if executa um bloco de código se uma condição for verdadeira. Se a condição for falsa, a estrutura é finalizada sem executar os comandos.

* A estrutura condicional composta if...else executa um bloco de código se uma condição for verdadeira. Se a
condição for falsa, outro bloco de código é executado e a estrutura é finalizada.

* A estrutura condicional composta if...elif...else é utilizada quando temos mais de uma condição no mesmo
bloco de estrutura condicional.

* Formatação numérica em Python:

        numero = 22345.54759
  
        # Exibe a variável número SEM FORMATAÇÃO:
        print('Número sem formatação: ', numero)
  
        # Exibe a variável número com separadores NO FORMATO AMERICANO:
        print(f'Número no formato americano: {numero:,}')
  
        # Exibe a variável número com separadores NO FORMATO AMERICANO com 2 casas decimais:
        print(f'Número no formato americano com 2 casas decimais: {numero:,.2f}')
  
        # Exibe a variável número com separadores NO FORMATO BRASILEIRO com 2 casas decimais:
        numero_em_texto = f"{numero:_.2f}"
        numero_em_texto = numero_em_texto.replace('.',',').replace('_','.')
        print('Número no formato brasileiro com 2 casas decimais:',numero_em_texto)
        print('Número no formato moeda brasileiro com 2 casas decimais: R$',numero_em_texto)

* Anotações:

Programa interpretado - Google Colab, Jupyter Notebook / Programa compilado - transforma o programa em código binário para ser gerado pela máquina.

-----------------

### **Aula 4 - Estruturas Condicionais**

* Estruturas condicionais servem para executar um conjunto de instruções várias vezes seguidas;

* Também conhecida como loop (laços).

* Um loop é executa repetidamente um conjunto de instruções enquanto determinada condição estiver sendo satisfeita.

* As principais estruturas de repetição no Python são o for e o while:

* WHILE: executa conjunto de instruções enquanto uma condição seja verdadeira. A condição de repetição deve ser definida logo no início do loop.

        while <condição>:
            <executar_instruções>
        else:
            <executar_outras_instruções>

* FOR: funciona em um conjunto de itens fixos, como faixa de dados (range()) ou tipos de dados iteráveis como listas.

        for <item> in <conjunto_de_itens>:
         <bloco_de_código>
  
-----------------

  ### **Aula 5 - Listas em Python**

* Uma lista em Python é uma coleção ordenada de valores. As listas contém valores separados por vírgula e dentro de colchetes []. Listas são utilizadas 
para armazenar diversos itens em uma única variável. Listas são objetos usados com frequência em análise de dados. Veja o exemplo de uma lista:

        Exemplo de lista: 
        estados_sudeste = ['ES', 'MG', 'RJ', 'SP']
        print(estados_sudeste)
        print(type(estados_sudeste))
        
        Saída: 
        ['ES', 'MG', 'RJ', 'SP']
        <class 'list'>

-------

* Listas - Inserindo itens em lista: 

list.append --> Adiciona um item ao fim de uma lista

list.insert --> Insere um item em uma posição index da lista

-------

* Listas – Removendo itens em uma lista

list.clear -> Apaga toda a lista

list.pop() --> remover um valor da lista definindo o ÍNDICE desejado

list.remove() --> remover um valor da lista definindo o VALOR da lista

método del --> mesmo resultado do pop

-------

* Listas – Outras operações com listas

list.index() --> para imprimir o índice quando não sabemos sua posição

list.count() --> conta a quantidade de vezes que um elemento/ valor aparece na lista

list.sort() --> (útil para ordenação de dados filtrados da web) - não funciona para listas contendo vários tipos de dados

list.reverse() --> reverte a ordem dos elementos de uma lista - não funciona para listas contendo vários tipos de dados

list.copy() --> Retorna uma lista com a cópia dos elementos da lista de origem -> ÚTIL PARA TESTES

-------

* Operadores min(), max(), sum() e len()

Em Python, as funções min(), max(), sum() e len() são comumente utilizadas com sequências de dados. As sequências mais comuns são:

Listas: Coleções ordenadas de itens, mutáveis e heterogêneas.
Tuplas: Coleções ordenadas de itens, imutáveis e heterogêneas.
Strings: Sequências de caracteres.
Cada função tem uma finalidade específica:

min(): Retorna o menor elemento de uma sequência.
max(): Retorna o maior elemento de uma sequência.
sum(): Calcula a soma de todos os elementos numéricos de uma sequência.
len(): Retorna o número de elementos de uma sequência.

--------

* Listas – Função range() --> Por padrão, os valores retornados na função range() são sequenciais e acrescidos de 1. Isso significa que, se utilizarmos o comando range(10), os valores retornados serão: '0, 1, 2, 3, 4, 5, 6, 7, 8 e 9'. Portanto, o valor inicial é zero e os números seguintes serão a somatória do valor atual mais 1.

--------

* Listas – List Comprehensions (Compreensão de Listas) --> List Comprehension é uma forma concisa de criar e manipular listas

				[expr for item in lista]

* Listas – List Comprehensions com if --> expressões condicionais para criar listas ou modificar listas existentes.

				[expr for item in lista if condição]

* Listas – List Comprehensions com if e else:
  
                       [resultado_if if expr else resultado_else for item in lista]

 -------

* Faixa de listas no Python (slicing ou list slice)

Sintaxe: (considere l uma lista qualquer)
1. l[inicio:parada]           # fatia a lista começando no index <inicio> até <parada-1>
2. l[inicio:]                 # fatia a lista começando no index <inicio> até o final da lista
3. l[:parada]                 # fatia a lista começando no index 0 até <parada-1>
4. l[:]                       # Considera toda a lista
5. l[inicio:parada:passo]     # fatia a lista começando no index <inicio> avançando em <passo>
                                # e não ultrapassando <parada>
6. l[-1]                      # último item da lista
7. l[-2:]                     # últimos dois itens da lista
8. l[:-2]                     # toda a lista, exceto os dois últimos itens
9. l[-inicio:-parada]         # fatia a lista começando no index <-inicio> até <-parada-1>

					# Exemplos
					lista = [0,1,2,3,4,5,6,7,8,9]
					print(lista[0:4])     # 1. saída [0, 1, 2, 3]
					print(lista[2:])      # 2. saída [2, 3, 4, 5, 6, 7, 8, 9]
					print(lista[:6])      # 3. saída [0, 1, 2, 3, 4, 5]
					print(lista[:])       # 4. [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
					print(lista[0:10:2])  # 5. [0, 2, 4, 6, 8]
					print(lista[-1])      # 6. saída 9
					print(lista[-2:])     # 7. saída [8, 9]
					print(lista[:-2])     # 8. saída [0, 1, 2, 3, 4, 5, 6, 7]
					print(lista[-5:-1])   # 9. saída [5, 6, 7, 8]

 -------
 
### **Aula 6 - Tuplas**

* Tuplas são uma sequência de objetos imutáveis, em outras palavras, uma vez criadas, tuplas não podem ser modificadas, normalmente são usadas para guardar dados protegidos.

* As tuplas são escritas entre parênteses ().
  
* Uma tupla em Python é semelhante a uma lista. A diferença entre os dois é que não podemos alterar os elementos de
uma tupla (IMULTÁVEL) depois de atribuída, enquanto que, podemos alterar os elementos de uma lista (MULTÁVEL)

* O acesso aos itens de uma tupla é idêntico ao de uma lista:

					linguagens = ("Python","Ruby","Javascript","Perl","Haskell")
					print(linguagens[0:2]) # ('Python', 'Ruby')
					print(linguagens[-1]) # Haskell
					print(linguagens[:-2]) # ('Python', 'Ruby', 'Javascript')

* As tuplas são úteis para representar o que outras linguagens costumam chamar de registros, algumas informações relacionadas que pertencem entre si, como o registro de um estudante. Uma tupla nos permite “agrupar” informações relacionadas e usá-las em uma única estrutura:

					estudante = ('Miguel', 29, 1990, 'Brasil')

* Agora podemos utilizar um for para imprimir todos os elementos da tupla estudante:
					
					for e in estudante:   # Percorre os valores da tupla estudante
					   print(e)           # Imprime os valores

* Também podemos facilmente converter esta tupla em uma lista usando a técnica list
comprehension:

					print([e for e in estudante]) # ['Miguel', 29, 1990, 'Brasil']

### **Aula 6 - Dicionários**

* Dicionários são uma coleção ordenada de pares de {chave : valor}, são normalmente usados quando temos uma grande quantidade de dados.
  
* Dicionários são otimizados para buscarmos dados e para isso, precisamos saber sua chave.
  
* Dicionários são definidos entre chaves {} onde cada item é um par na forma de {chave : valor}, separados por vírgulas sendo a chave e o valor podendo ser de qualquer tipo.
  
**Chaves:**

* Devem ser únicas;

* Tipos int, float, string, tuple, bool, é recomendável não utilizar o tipo float como chave;

* Nenhuma ordem para chaves ou valores.

**Valores:**

* Qualquer tipo;
  
* Pode ser duplicado;
  
* Valores de dicionários podem ser listas, até mesmo outros dicionários

					elemento = {
					    'nome': 'Ouro',
					    'símbolo': 'Au',  # Corrigido o fechamento das aspas
					    'número atômico': 79
					}
  
