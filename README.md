# fatorial

## Apresentação

Programa escrito em [Potigol](http://potigol.github.io) 🦐 para determinar o valor de um número fatorial.

### Pergunta motivacional
> 🤔 Será que é possível explicar, para uma professora de Língua Portuguesa, como o computador calcula o fatorial de um número usando a sintaxe do [Potigol](http://potigol.github.io)?

Esta pergunta surgiu nos meus pensamentos em uma [rápida conversa](https://twitter.com/cannudo_/status/1664742081430970368) que tive com uma das minhas professoras do Ensino Médio.

### Como fazer isso?
Pretendo fazê-lo escrevendo a lógica do cálculo fatorial e explicando, passo-a-passo, como o computador vai processar o código-fonte gerado. A escolha do Potigol se deu por ser uma linguagem escrita em Português do Brasil e por ela suportar a programação estruturada.

## Definições, perguntas e respostas

### Definição de fatorial
O fatorial de um número <var>n</var> é o produto dos números naturais consecutivo de 1 até <var>n</var>.

É representado por um número inteiro seguido por um ponto de exclamação.

#### Exemplo
_Quanto é 5! (cinco fatorial)?_
> 5! = 5 · 4 · 3 · 2 · 1 = 120 (cinco fatorial é igual a cento e vinte, pois cento e vinte é o produto dos números naturais de um um até cinco).

### Antes de começar
Algumas perguntas podem surgir imediatamente após se ler a definição de fatorial. Por exemplo:

_Quando se quer saber o fatorial de 0, como faz? Fatorial de 1? Existe fatorial de número negativo?_
> Seja <var>n</var> o número do qual se deseja descobrir o fatorial, <var>n</var> deve ser maior ou igual a 0 (n ≥ 0). Ou seja: _não existe fatorial de números negativos._ Caso <var>n</var> seja 0 ou 1, o fatorial de <var>n</var> é 1.

💡 Essas respostas serão importantes na construção do programa.

## Execução local

### Instruções para execução do código
Assumindo que você já tenha [instalado o Potigol](https://potigol.github.io/docs/instalacao/) na sua máquina, digite na linha de comandos (usando Debian GNU/Linux):
```terminal
java -jar potigol.jar fatorial.poti
```