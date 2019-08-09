import time
from random import randint
import timeit
import matplotlib as mpl
import matplotlib.pyplot as plt


def desenhaGrafico(x,y,y2,xl = "Entradas", yl = "Saídas"):
    fig = plt.figure(figsize=(10, 8))
    ax = fig.add_subplot(111)
    ax.plot(x,y, label = "Tempo no caso qualquer")
    ax.plot(x,y2, label = "pior Tempo")
    ax.legend(bbox_to_anchor=(1, 1),bbox_transform=plt.gcf().transFigure)
    plt.ylabel(yl)
    plt.xlabel(xl)
    plt.show()
    
    
def desenhaGrafico2(x,z,z2,xl = "Entradas", yl = "Saídas"):
    fig = plt.figure(figsize=(10, 8))
    ax = fig.add_subplot(111)
    ax.plot(x,z, label = "operaçoes no caso qualquer")
    ax.plot(x,z2, label = "operaçoes no pior tempo")
    ax.legend(bbox_to_anchor=(1, 1),bbox_transform=plt.gcf().transFigure)
    plt.ylabel(yl)
    plt.xlabel(xl)
    plt.show()
    
def geraLista(tam):
    lista = []
    for i in range(tam):
        n = randint(1,1*tam)
        if n not in lista: lista.append(n)        
    return lista
    
    
def geraLista2(tam):
    lista = []
    for i in range(tam,0,-1):
        lista.append(i)
    return lista
    
       
x2 = [10000,20000,50000,100000]
y = []
y2= []
z = []
z2=[]



def sort(array):
    r=0
    inicio = timeit.default_timer()
    for p in range(0, len(array)):
        current_element = array[p]

        while p > 0 and array[p - 1] > current_element:
            array[p] = array[p - 1]
            p -= 1
            r=r+1

        array[p] = current_element

    z.append(r)
    fim = timeit.default_timer()
    y.append('%f' %(fim - inicio))


def sort2(array):
    r=0
    inicio = timeit.default_timer()
    for p in range(0, len(array)):
        current_element = array[p]

        while p > 0 and array[p - 1] > current_element:
            array[p] = array[p - 1]
            p -= 1
            r=r+1

        array[p] = current_element
        
    z2.append(r)
    fim = timeit.default_timer()
    y2.append('%f' %(fim - inicio))


for i in range(4):
    array = geraLista(x2[i])
    sort(array)
    array2 = geraLista2(x2[i])
    sort2(array2)
    print(z)
    print(z2)


desenhaGrafico(x2,y,y2)
desenhaGrafico2(x2,z,z2)



  
