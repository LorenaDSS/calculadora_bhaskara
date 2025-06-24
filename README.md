Calculadora de Bhaskara - Visualg
Este é um algoritmo feito em Portugol (Visualg) para calcular as raízes de uma equação do segundo grau utilizando a Fórmula de Bhaskara.

## Código:

```portugol
Algoritmo "Fórmula de Bhaskara"

Var
    a, b, c: inteiro
    delta, raiz_de_delta, valor_b_negativo, positivo, negativo, x1, x2: real

Inicio
    escreval("===== Calculadora de Bhaskara =====")
    escreval()

    escreval(" Digite o coeficiente a: ")
    leia(a)

    escreval(" Digite o coeficiente b: ")
    leia(b)

    escreval(" Digite o coeficiente c: ")
    leia(c)

    escreval()
    escreval("=============================================")
    escreval()

    delta <- b^2 - 4*a*c

    se delta < 0 entao
        escreval(" Delta é negativo e não existem raízes reais.")
        escreval()
        escreval("=============================================")
    senao
        raiz_de_delta <- raizq(delta)
        valor_b_negativo <- -b
        positivo <- valor_b_negativo + raiz_de_delta
        negativo <- valor_b_negativo - raiz_de_delta
        x1 <- positivo / (2*a)
        x2 <- negativo / (2*a)

        se x1 = x2 entao
            escreval(" Delta é nulo, X1 e X2, são duas raízes reais e iguais que valem: ", x1)
            escreval()
            escreval("=============================================")
        senao
            escreval(" Delta = ", delta)
            escreval(" Raiz Quadrada de Delta = ", raiz_de_delta)
            escreval()
            escreval(" Delta é positivo e as duas raízes são reais e diferentes:")
            escreval(" X1 =", x1)
            escreval(" X2 =", x2)
            escreval()
            escreval("=============================================")
        fimse
    fimse

Fimalgoritmo
