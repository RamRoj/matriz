#Multiplicacion de matries
#coding:utf8
import sys
import os
A=[]
B=[]
C=[]
i=1
while i==1:
    os.system('cls')
    sys.stdin.flush()
    orden=int(raw_input("\n\tIngrese el orden de las matrices: "))

#Matriz A
    for x in range (0,orden):
        A.append([0]*orden)  #creo el numero de elemtnos de cada vector fila
    os.system('cls')
    for filas in range (0,orden):
        for columnas in range (0,orden):
            A[filas][columnas]=int(raw_input('\n\n\tIngrese el elemento A[%d][%d]: '%(filas+1,columnas+1)))


#Matriz B
    for x in range (0,orden):
        B.append([0]*orden)  #creo el numero de elemtnos de cada vector fila
    os.system('cls')
    for filas in range (0,orden):
        for columnas in range (0,orden):
            B[filas][columnas]=int(raw_input('\n\tIngrese el elemento B[%d][%d]: '%(filas+1,columnas+1)))

#Matriz C
    for x in range (0,orden):
        C.append([0]*orden)  #creo el numero de elemtnos de cada vector fila
    os.system('cls')


#Opcion de suma o multiplicacion
    opc=int(raw_input('\n\n\tIngrese la opcion:\n\n\tMultiplicacion: 1\n\n\tSuma: 2\n\n\tSalir: 3\n\n\t>>  '))

#Multiplicacion
    if opc==1:
        os.system('cls')
        for filas in range (0,orden):
            for columnas in range (0,orden):
                for aux in range (0,orden):
                    C[filas][columnas]+=A[filas][aux]*B[aux][columnas]

#Suma
    elif opc==2:
        os.system('cls')
        for filas in range (0,orden):
            for columnas in range (0,orden):
                C[filas][columnas]=A[filas][columnas]+B[filas][columnas]

#Salir
    elif opc==3:
        os.system('cls')
        print'\n\tHasta Luego'
        sys.exit()


#Imprime Resultados
    print"\nLa matriz A es:"
    for x in range (0,orden):
        print A[x]

    print"\nLa matriz B es:"
    for x in range (0,orden):
        print B[x]

    print '\n\n'
    print"\nEl resultadonde es:"
    for x in range (0,orden):
        print C[x]
        print "\n"
    i=int(raw_input("\n\tIngrese '1' para volver a calcular o cualquier otra tecla para salir.\n\n\t>> "))
