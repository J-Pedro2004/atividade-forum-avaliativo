# Análise e Refatoração de Algoritmo

**Disciplina / Atividade:** Algoritmo e Programação / Fórum Avaliativo

**Tema:** Escalabilidade e Estruturas de Repetição em Pseudocódigo

## 1. Análise do Problema

O algoritmo original apresenta um problema de escalabilidade, pois utiliza variáveis e operações fixas para armazenar e somar as notas de apenas 5 alunos.

Se a turma tivesse 100 alunos, seria necessário criar mais variáveis, repetir os comandos de leitura e aumentar a operação de soma, tornando o código extenso e difícil de manter.

A solução é utilizar uma estrutura de repetição, permitindo processar uma quantidade variável de notas sem precisar modificar o código.

## 2. Algoritmo Refatorado

A refatoração foi realizada utilizando a estrutura de repetição `ENQUANTO`, permitindo a leitura de uma quantidade variável de notas.

O algoritmo também possui validação das notas informadas e utiliza o valor `-1` para encerrar a entrada de dados.

O código-fonte completo está disponível no arquivo [`CalculaMediaTurmaDinamica.por`](./CalculaMediaTurmaDinamica.por).

## 3. Vantagens da Solução

- **Menos variáveis:** utiliza apenas uma variável para receber as notas, independentemente da quantidade de alunos.
- **Flexibilidade:** permite processar turmas de diferentes tamanhos sem alterar o código.
- **Validação:** impede que notas fora do intervalo de 0 a 10 sejam utilizadas no cálculo.
- **Organização:** evita comandos repetitivos e facilita a manutenção do algoritmo.

## Conclusão

A utilização da estrutura de repetição `ENQUANTO` resolveu o problema de escalabilidade do algoritmo original. Com essa alteração, o programa consegue processar diferentes quantidades de alunos de maneira mais simples, organizada e eficiente.
