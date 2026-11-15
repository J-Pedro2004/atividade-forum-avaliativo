# Análise e Refatoração de Algoritmo

**Disciplina / Atividade:** Fórum Avaliativo

**Tema:** Escalabilidade e Estruturas de Repetição em Pseudocódigo

## 1. Análise do Problema

O algoritmo original apresenta um problema de escalabilidade, pois utiliza variáveis e operações fixas para armazenar e somar as notas de apenas 5 alunos.

Se a turma tivesse 100 alunos, seria necessário criar mais variáveis, repetir os comandos de leitura e aumentar a operação de soma, tornando o código extenso e difícil de manter.

A solução é utilizar uma estrutura de repetição, permitindo processar uma quantidade variável de notas sem precisar modificar o código.

## 2. Algoritmo Refatorado

A solução utiliza a estrutura `ENQUANTO` para realizar a leitura das notas. O valor `-1` funciona como sentinela, indicando o encerramento da entrada de dados.

Também foi implementada uma validação para aceitar somente notas entre 0 e 10.

```portugol
Algoritmo "CalculaMediaTurmaDinamica"

Var
   notaAtual, soma, media: Real
   totalAlunos: Inteiro

Inicio
   soma <- 0
   totalAlunos <- 0

   Escreval("Digite as notas dos alunos.")
   Escreval("Digite -1 para encerrar.")

   Escreva("Nota do aluno ", totalAlunos + 1, ": ")
   Leia(notaAtual)

   Enquanto (notaAtual <> -1) Faca

      Se (notaAtual >= 0) e (notaAtual <= 10) Entao
         soma <- soma + notaAtual
         totalAlunos <- totalAlunos + 1
      Senao
         Escreval("Nota inválida! Digite um valor entre 0 e 10.")
      FimSe

      Escreva("Nota do próximo aluno (ou -1 para encerrar): ")
      Leia(notaAtual)

   FimEnquanto

   Se (totalAlunos > 0) Entao
      media <- soma / totalAlunos

      Escreval("Total de alunos: ", totalAlunos)
      Escreval("Média da turma: ", media:4:2)
   Senao
      Escreval("Nenhuma nota válida foi informada.")
   FimSe

Fimalgoritmo
```

## 3. Vantagens da Solução

- **Menos variáveis:** utiliza apenas uma variável para receber as notas, independentemente da quantidade de alunos.
- **Flexibilidade:** permite processar turmas de diferentes tamanhos sem alterar o código.
- **Validação:** impede que notas fora do intervalo de 0 a 10 sejam utilizadas no cálculo.
- **Organização:** evita comandos repetitivos e facilita a manutenção do algoritmo.

## Conclusão

A utilização da estrutura de repetição `ENQUANTO` resolveu o problema de escalabilidade do algoritmo original. Com essa alteração, o programa consegue processar diferentes quantidades de alunos de maneira mais simples, organizada e eficiente.
