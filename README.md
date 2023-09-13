# ac3
ac3
#1
salário_atual = float(input("digite o salário atual do colaborador: R$ "))

faixas_reajuste = [(0, 400.00, 15), (400.01, 800.00, 12), (800.01, 1200.00, 10), (1200.01,2000.00, 7)]

percentual_aumento = 0

for faixa in faixas_reajuste:
    if salário_atual >= faixa[0] and salário_atual <= faixa[1]:
        percentual_aumento = faixa[2]
        break

aumento =(salário_atual * percentual_aumento) / 100

salário_novo = salário_atual + percentual_aumento


print("\nReajuste salarial: ")
print("Salário pre reajuste: R$ {:.2f}".format(salário_atual))
print("Perceuntual de aumento: {}%".format(percentual_aumento))
print("quantidade do aumento: R$ {:.2f}".format(aumento))
print("Salário novo: R$ {:.2f}".format(salário_novo))



#2

def dia_da_semana(número):
    if número == 1:
        return "DOMINGO"
    elif número == 2:
        return "SEGUNDA"
    elif número == 3:
        return "TERÇA"
    elif número == 4:
        return "QUARTA"
    elif número == 5:
        return "QUINTA"
    elif número == 6:
        return "SEXTA"
    elif número == 7:
        return "SABADO"
    else: "número invalido, insira um número de 1 a 7"


try:
    número = int(input("Insira um número de 1 a 7: "))
    resultado = dia_da_semana(número)
    print("dia da semana: ", resultado)
except ValueError:
    print("Insira um número válido")


#3
import math

a = float(input("valor de a"))
if a == 0:
    print("valor de a não pode ser zero. A equação não é de segundo grau")
else:
    b = float(input("valor de b: "))
    c = float(input("valor de c: "))

    delta = b**2 -4*a*c


    if delta < 0:
        print("Equação não possui raizes reais, delta é negativo")
    elif delta == 0:
        raiz= -b / (2*a)
        print(f"Equação possui raiz real: {raiz}")
    else:
        raiz1 = (-b + math.sqrt(delta)) / (2*a)
        raiz2 = (-b - math.sqrt(delta)) / (2*a)
        print(f"Equação tem duas raízes reais:")
        print(f"raiz 1: {raiz1}")
        print(f"raiz 2: {raiz2}")
