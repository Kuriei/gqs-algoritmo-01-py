# gqs-algoritmo-01-py
Sobre o projeto:

Este projeto foi feito para analisar se uma frase é um palíndromo.

A função analisar(entrada) recebe um texto, remove os caracteres que não são letras ou números, coloca tudo em letras minúsculas e depois verifica se o texto é igual ao seu inverso.

Nível 1
O que o código faz?
O principal objetivo da função analisar é verificar se a entrada é um palíndromo.
Um palíndromo é uma palavra ou frase que pode ser lida da mesma forma de trás para frente.

Exemplo:
ovo
Ao inverter, continua sendo:
ovo

Por isso, o resultado seria True.

Como executar?

O projeto disponibilizado está em Python (.py).
Primeiro, é necessário ter o Python instalado. Depois, pelo terminal, entre na pasta do projeto e execute:

python DesafioLogica.py

Em alguns computadores pode ser necessário usar:

python3 DesafioLogica.py

Observação

A atividade menciona os comandos javac e java, porém o arquivo disponibilizado pelo professor é Python. Por isso, utilizei o comando do Python para executar o programa.

Exemplo de saída

Ao executar o programa, são apresentados os seguintes resultados:

Teste 1: False
Teste 2: True

Nivel 2:

Análise dos métodos

Método main

O código não possui um método main() como normalmente existe em Java.

No Python, existe a seguinte estrutura:

if __name__ == "__main__":

Ela faz com que os testes sejam executados quando o arquivo é executado diretamente.

Nesse trecho, são criados dois textos e a função analisar() é chamada para cada um deles.

Método analisar(entrada)

A função começa verificando se a entrada é None:

if entrada is None:
    return False

Se não existir uma entrada, o resultado será False.

Depois, o código limpa o texto:

limpa = re.sub(r'[^a-zA-Z0-9]', '', entrada).lower()

O re.sub remove os caracteres que não são letras ou números.

Por exemplo, espaços, vírgulas e hífens são removidos.

O .lower() transforma todas as letras em minúsculas.

Depois disso, o programa cria uma versão invertida:

invertida = limpa[::-1]

O [::-1] é uma forma de inverter uma string em Python.

Por fim:

return limpa == invertida

O programa compara o texto original com o texto invertido. Se forem iguais, retorna True; caso contrário, retorna False.

Análise dos testes

Teste 1

A sacada da casa de cadasa

O resultado foi:

Teste 1: False

Isso acontece porque, depois que o texto é limpo e invertido, ele não fica igual ao texto original.

Portanto, não é considerado um palíndromo pelo programa.

Teste 2

Socorram-me, subi no ônibus em Marrocos

O resultado foi:

Teste 2: True

Depois da limpeza, o texto pode ser lido igualmente nos dois sentidos.

Por isso, a comparação entre o texto e seu inverso resulta em True.

Código analisado

import re

def analisar(entrada):
    if entrada is None:
        return False

    limpa = re.sub(r'[^a-zA-Z0-9]', '', entrada).lower()

    invertida = limpa[::-1]

    return limpa == invertida

Nível 3

Uso de Markdown

O README utiliza títulos, listas e blocos de código para organizar a documentação.

Sobre o autor

Nome: [SEU NOME]

RA: 32516918

Matéria: Garantia da Qualidade de Software.
