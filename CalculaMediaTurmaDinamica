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
