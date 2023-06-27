# Isolamento de erro: fatorial de números maiores que 12

Nos testes manuais, percebeu-se que o fatorial de números grandes não é retornado como esperado.

## ✔️ Comportamento esperado
```terminal
• • • calculadora de fatorial • • •
Digite um número inteiro: 50
50! = 30414093201713378043612608166064768844377641568960512000000000000
```

## ⚠️ O que rola
```terminal
• • • calculadora de fatorial • • •
Digite um número inteiro: 50
50! = 0
```

(doguinho Caramelo)

Em uma jornada exploratória, descobriu-se também que:
* Para números menores que 50, o retorno não é 0. Mesmo assim, não é o valor correto. Veja, por exemplo, com 13:
```terminal
• • • calculadora de fatorial • • •
Digite um número inteiro: 13
13! = 1932053504
```
* O limite para o cálculo correto é 12:
```terminal
• • • calculadora de fatorial • • •
Digite um número inteiro: 12
12! = 479001600
```

## Técnicas utilizadas
Para isolar o erro, mudou-se algumas coisas no código.
* Em primeiro lugar, as linhas referentes à entrada do valor em questão foram removidas;
* Então, foi inclusa uma atribuição de valor manual. Dessa forma, poderemos apenas rodar o código e comparar a saída com o valor esperado;
* O valor atribuido foi 13, por ser um incremento direto do limite para o cálculo correto.

## Execução dos testes
Assumindo que você já tenha instalado o Potigol, digite na linha de comandos (usando Debian GNU/Linux):
```terminal
java -jar potigol.jar fatorial.poti
```

## ✔️ Comportamento esperado
```terminal
• • • calculadora de fatorial • • •
13! = 6227020800
```

## ✅ Solução
Após uma pesquisa no código-fonte do Potigol, constatou-se que o erro se dá pelo tamanho do número do resultado que, por ser muito grande, não é suportado por padrão pelo Potigol.

A solução consiste na declaração de um tipo numérico que suporta um valor maior, que o Potigol pega eprestado da linguagem [Scala](https://www.scala-lang.org/): o _BigInt_.

Nó código-fonte ```fatorial.poti```, as principais mudanças são:

```potigol
tipo InteiroGrande = BigInt

fatorial(numero: InteiroGrande): InteiroGrande =
```

O  código completo da solução está neste commit e está sujeito à decisão final do autor, uma vez que estes detalhes são mais técnicos e não agregam tanto valor para o objetivo final: explicar como o computador calcula o fatorial de um número.