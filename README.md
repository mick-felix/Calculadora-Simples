# Calculadora Simples em C

Este é um projeto de console simples, desenvolvido como parte de um estudo aprofundado dos conceitos fundamentais da linguagem C. O programa solicita ao usuário dois números e um operador aritmético para realizar um cálculo básico.

## Especificações Técnicas

O programa foi projetado para seguir um fluxo claro e robusto de interação com o usuário:

* **Entrada de Dados:**
    1.  Solicita um primeiro número do tipo `float`.
    2.  Solicita um operador aritmético do tipo `char` (`+`, `-`, `*`, `/`).
    3.  Solicita um segundo número do tipo `float`.

* **Processamento:**
    * O programa utiliza uma estrutura condicional (`if/else if/else`) para determinar qual operação matemática deve ser executada com base no operador fornecido.
    * A lógica de cada operação matemática é encapsulada em sua própria função (`somar`, `subt`, `mult`, `divisao`).
    * Inclui uma verificação de erro específica para o caso de **divisão por zero**, interrompendo a execução e informando o usuário antes que o cálculo problemático ocorra.

* **Saída de Dados:**
    * Exibe o resultado final da operação formatado com duas casas decimais.
    * Em caso de erro (como divisão por zero), exibe uma mensagem clara informando o problema.

## Tecnologias Utilizadas

* **Linguagem:** C (Padrão C11)
* **Biblioteca Padrão:** `stdio.h` (Standard Input/Output Library) para as funções de entrada (`scanf`) e saída (`printf`).
* **Compilador:** O código é compatível com compiladores padrão como `GCC` e `Clang`.
* **Ambiente de Desenvolvimento:** Visual Studio Code, com auxílio de snippets personalizados para agilizar a codificação.

## O que aprendi com este Projeto

Este projeto foi um exercício prático fundamental que solidificou diversos conceitos essenciais da programação em C:

1.  **Modularização com Funções:**
    * Aprendi a separar responsabilidades no código. A função `main` ficou encarregada do fluxo e da interação com o usuário, enquanto funções especialistas (`somar`, `divisao`, etc.) ficaram responsáveis apenas pelos cálculos.
    * Entendi na prática como declarar **protótipos de funções** no início do arquivo para organizar o código e manter a `main` como a primeira função a ser lida.

2.  **Tratamento de Entrada de Dados:**
    * Aprofundei meu conhecimento sobre `scanf`, especialmente ao lidar com a leitura de tipos de dados diferentes em sequência.
    * Compreendi o desafio do **buffer de entrada** e aprendi a técnica de usar um espaço antes do `%c` (`scanf(" %c", ...);`) para consumir caracteres de espaço em branco (como o `\n` deixado pela leitura anterior) e evitar bugs.

3.  **Lógica Condicional e Depuração (Debugging):**
    * Reforcei o uso de `if / else if / else` para controlar o fluxo do programa.
    * Aprendi a importância da diferença entre **literais de caractere** (`'+'`) e **literais de string** (`"+"`) em comparações.
    * Entendi a diferença crucial entre um **valor numérico** (`0`) e um **caractere** (`'0'`), um erro comum que consegui identificar e corrigir durante o desenvolvimento.

4.  **Boas Práticas de Código:**
    * **Separação de Responsabilidades:** A decisão de colocar a validação da divisão por zero na `main` (a função "chefe") em vez de na função `divisao` (a "especialista") foi uma lição importante sobre design de software, tornando as funções de cálculo mais puras e reutilizáveis.
    * **Código Limpo:** Utilizei nomes de variáveis claros e adotei a prática de comentar o código com cabeçalhos de arquivo e de função, tornando-o mais legível e fácil de manter.
