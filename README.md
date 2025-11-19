class Nodo:
    def __init__(self,valor):
        self.valor = valor  
        self.izquierda = None
        self.derecha = None


nodo_10 = Nodo(10)
nodo_1 = Nodo(1)
nodo_3 = Nodo(3)
nodo_20 = Nodo(20)
nodo_3 = Nodo(3)
nodo_2 = Nodo(2)

nodo_suma_abajo = Nodo("+")
nodo_suma_abajo.izquierdo=nodo_10
nodo_suma_abajo.derecha=nodo_1
nodo_multiplicacion_abajo = Nodo("*")
nodo_multiplicacion_abajo.izquierda = nodo_suma_abajo
nodo_multiplicacion_abajo.deracha =nodo_3 
nodo_resta_abajo = Nodo("-")
nodo_resta_abajo.izquierda=nodo_multiplicacion_abajo
nodo_resta_abajo.derecha=nodo_20
nodo_suma_raiz=Nodo("+") 
nodo_multiplicacion_abajo=Nodo("*")
nodo_multiplicacion_abajo.izquierda=nodo_3
nodo_multiplicacion_abajo.derecho=nodo_2



def recorrido_in(raiz):
    if raiz:
        recorrido_in(raiz.izquierda)
        print(raiz.valor, end=" ")
        recorrido_in(raiz.derecha)


def recorrido_pre(raiz):
    if raiz:
        print(raiz.valor, end=" ")
        recorrido_pre(raiz.izquierda)
        recorrido_pre(raiz.derecha)


def recorrido_pos(raiz):
    if raiz:
        recorrido_pos(raiz.izquierda)
        recorrido_pos(raiz.derecha)
        print(raiz.valor, end=" ")

print("IN_ORDEN")
recorrido_in(raiz)
print(" ")
print("PRE_ORDEN")
recorrido_pre(raiz)
print(" ")
print("POS_ORDEN")
recorrido_pos(raiz)
