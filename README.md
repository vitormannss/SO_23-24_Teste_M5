# Teste de Sistemas Operativos - Módulo 5

Faz *fork* do repositório para teres a tua cópia.

Preenche o ficheiro README diretamente no GitHub. A partir da página principal do repositório, clica em "Edit File" (ícone representando um lápis).

Escreve as respostas dentro dos blocos correspondentes. Substitui as reticências pelo que é pedido em cada pergunta. Não desformates o documento.

Quando acabares, carrega no botão "Commit Changes".

## Informação do aluno

    Nome: Vitor Santos  11Q1

## P1 - Para as seguintes questões, assinala a opção correta: (2.5v)

  1. Que comando é usado para definir permissões de execução num script Bash?

    A) chmod +x script.sh
    B) chmod -x script.sh
    C) chmod +r script.sh
    D) chmod -r script.sh
    
    Resposta: A)

  2. Como se define um comentário num script Bash?

    A) // comentário
    B) /* comentário */
    C) # comentário
    D) -- comentário
    
    Resposta: C)
   
  3. Que comando é usado para adicionar uma linha de texto ao final de um arquivo em Bash?

    A) echo "texto" > arquivo
    B) echo "texto" < arquivo
    C) echo "texto" | arquivo
    D) echo "texto" >> arquivo
    
    Resposta: D)

  4. Qual é o comando usado para ler a entrada do utilizador num script Bash?

    A) read
    B) input
    C) get
    D) scan
    
    Resposta: A)

  5. Que símbolo é usado para denotar uma variável em Bash?

    A) %
    B) $
    C) &
    D) #
    
    Resposta: B)

## P2 - Escreve scripts em Bash para realizar as seguintes instruções: (7.5v)

  1. Exibir a mensagem "Olá, Mundo!" no terminal.

    Resposta:
    ```bash
    #!/bin/bash
    echo "Olá, Mundo!"
    ```

    
  2. Receber dois números como entrada, e exibir a soma dos dois.

    Resposta:
    ```bash
    #!/bin/bash
    echo "Digite o primeiro número:"
    read num1
    echo "Digite o segundo número:"
    read num2
    soma=$((num1 + num2))
    echo "A soma dos dois números é: $soma"
    ```


  3. Ler um valor numérico e imprimir uma mensagem a informar se o mesmo é par ou ímpar.

    Resposta:
    ```bash
    #!/bin/bash
    echo "Digite um número:"
    read numero
    if ((numero % 2 == 0)); then
    echo "O número $numero é par."
    else
    echo "O número $numero é ímpar."
    fi
    ```


## P3 - Indica o que é realizado pelas seguintes instruções: (6v)

  1. 
    
    echo "scale=2;22/7" | bc

    Resposta:
Este comando calcula a divisão de 22 por 7 com precisão de duas casas decimais. O `bc` é um calculador de precisão arbitrária e `scale=2` define que o resultado deve ter duas casas decimais. A saída será `3.14`.

     
  2. 
    
    #!/bin/bash
    sum=0
    for i in {1..5}
    do
      sum=$((sum + i))
    done
    echo "A soma dos números de 1 a 5 é $sum."


    Resposta:
   
Este script calcula a soma dos números de 1 a 5. Ele inicializa a variável `sum` com 0, e para cada valor de `i` no intervalo de 1 a 5, adiciona `i` à `sum`. Ao final, exibe "A soma dos números de 1 a 5 é 15".


  3. 
    
    #!/bin/bash
    num=10
    while [ $num -gt 0 ]
    do
      echo "Número: $num"
      ((num--))
    done

    Resposta:
Este script exibe uma contagem decrescente de 10 até 1. Inicializa a variável `num` com 10 e, enquanto `num` for maior que 0, imprime o valor de `num` e decrementa `num` em 1 a cada iteração do loop `while`.


## P4 - Realiza os seguintes exercícios, com respostas detalhadas: (4v)

  1. O que é um **shebang** (#!) e qual é a sua função num script?

    Resposta:
    O **shebang** (`#!`) é uma sequência de caracteres colocada no início de um script. Sua função é indicar ao sistema operativo qual interpretador deve ser usado para executar o script. Por exemplo, `#!/bin/bash` especifica que o script deve ser executado usando o interpretador Bash. O shebang facilita a execução do script sem precisar invocar explicitamente o interpretador.


  2. Como se utiliza a instrução 'if-else' num script Bash? Escreve um exemplo simples.

    Resposta:
    ```bash
    #!/bin/bash
    echo "digite um número:"
    read numero
    if [ $numero -gt 0 ]; then
    echo "o número $numero é positivo."
    elif [ $numero -lt 0 ]; then
    echo "o número $numero é negativo."
    else
    echo "ox     número é zero."
    fi
    ```

