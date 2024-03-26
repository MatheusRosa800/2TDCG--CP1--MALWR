# FIAP - 1° Checkpoint - Análise de Malware

## Introdução
Checkpoint realizado com o intuito de colocar em prática todos os conhecimentos sobre análise de malwares na matéria de Malware Analysis, ministrada pelo [Professor Charles Lomboni](https://www.linkedin.com/in/charleslomboni/).

## Feito por

- Matheus Rosa

## Credenciais usadas para solução

USER: matheusrosa

PASS: mat-eusrosa

# Write Up

## 1. DIE

Utilizei o DIE para ver mais informações osbre o executavel, ver sua estrutura e se havia proteções.

Imagem do programa
<img src="Imagens/Imagem1.png">

## 2. Abri pelo CMD

Como o programa fechava e nem se quer mostrava alguma mensagem de erro, abri pelo cmd.

Imagem do programa

## 3. Abri o x32dbg e procurei pela a string de erro mostrada no cmd

IMagem das strings

## 4. Breakpoints para ir analisando instrução por instrução

Imagem Breakpoints

## 5. Primeira Analise

Logo depois de inserir a senha ele pula para uma função que compara a entrada do user com o valor B 

Transformando em decimal, seria 11. 

Logo, a entrada do user precisa ter 11 caracteres. 

Imagem do CMP B

## 5. Segundo erro

testando com uma senha de 11 caracteres e chutandoa a senha aparece esse erro 

Imagem Erro 2 

Fazendo a mesma coisa de ir atras da string e tal encontrei duas validações

## 7. Segunda Analise

Ao inserir a senha o valor vai diretamente para eax

e depois vem a primeira validação 

## 8. LOOP

faz um loop que 
compara eax com edi 
e incrementa o edi ate ficarem iguais

Segunda validação 

compara eax+3 com 2D 
2D em ascii é ifen(-)
sendo eax matheusrosa
eax+3 seria eusrosa
o quarto caracter precisa ser um ifen - 

