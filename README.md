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

### **Aula 3 - Estruturas Condicionais**

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
