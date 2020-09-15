"""
Created on Sun Sep 13 15:08:12 2020
@author: Murilo Trevisan
"""

import math
import numpy as np

# Intervalo de cálculo da raíz    
a = -1
b = 0

# Lista para armazenar os valores das iterações
x = [a]

# Erro da solução
e = 0.000001

# Número máximo de iterações
Maxiter = 10
k=0

# Definição da função a ser usada
def f(x):
    return 21*x**4 - 11*x**3 + 19*x**2 - 11*x - 2

# Teste se o intervalo inferior é raíz
if f(a) == 0:
    print("A raíz vale:", a)

# Teste se o intervalo superior é raíz
elif f(b) == 0:
    print("A raíz vale:", b)

# Teste se há raíz no intervalo    
elif f(a)*f(b) > 0:
    print("Não há raíz no intervalo")

# Teorema de bolzano:
elif f(a) * f(b) < 0:
   print("há uma raiz no intervalo", a, b)
   
   # Iterações
   for k in range(1 , Maxiter):
       x.append((a+b)/2)
       print("Iteração =", k, "Valor de a:", a, "Valor de b:", b, "Valor de Xk:", x[k], " O valor de f(x) =", f(x[k]) )
       # Teste se o valor médio é a raiz
       if f(x[k]) == 0:
           print("A raíz de f(x) =", x[k])
           break
       # Teste se o valor médio é próximo o suficiente da raíz dado um erro
       elif abs(x[k] - x[k-1]) < e * max(1, abs(x[k])):
           print("O valor da raíz aproximada é:", x[k])
           break
       # Teste se a raíz esta no intervalo inferior ao valor médio
       elif f(x[k])*f(a) < 0:
           b = x[k]
       # teste se a raíz esta no intervalo superior ao valor médio   
       elif f(x[k])*f(b) < 0:
           a = x[k]
           
       else:
           print("Erro 2")
       
else:
    print("Erro 1")
