# Fatorial de um número — 🖥️🧠 como o computador deve pensar?

## Introdução

Caríssimos leitores, obrigado pelo interesse neste projeto que foi motivado pela busca de respostas para a seguinte pergunta:

> Será que é possível explicar para um(a) professor(a) de Língua Portuguesa como um computador, que se propõe a resolver um cálculo matemático — o *fatorial* —, deve pensar para atingir tal objetivo?

Em outra perspectiva, como o computador deve ser programado para calcular o fatorial de um número?

Esta pesquisa é importante para que se possa ter uma ideia sobre se é possível que uma pessoa não-programadora entenda como os computadores pensam caso as instruções de processamento sejam escritas em um idioma mais natural ao seu dia-a-dia.

🤗 Sejam todes muito bem-vindes. Sintam-se à vontade para consumir este material da forma que quiserem. Discussões, troca de ideias e sugestões são apreciadas.

## Desenvolvimento

```potigol
fatorial(numero: Inteiro): Inteiro =
    se (numero == 0 ou numero == 1) entao
        1
    senão
        numero * fatorial(numero - 1)
    fim

escreva("• • • calculadora de fatorial • • •")
imprima("Digite um número inteiro (0-12): ")
numero = leia_inteiro
se (numero < 0) então
    escreva("{numero} é um número negativo. Não existe fatorial de números negativos.")
senão
    se (numero > 12)
        escreva("Número acima do limite suportado.")
    senão
        escreva("{numero}! = {fatorial(numero)}")
    fim
fim
```

## Conclusão