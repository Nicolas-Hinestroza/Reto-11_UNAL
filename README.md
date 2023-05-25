# Reto-11_UNAL
Desarrolle la mayoría de ejercicios en clase, por cado punto resuelto en clase tendrá media décima en el examen 2 (creanme, las van a necesitar). Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_11 en slack.

- **1. Desarrolle un programa que permita realizar la suma/resta de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.**

![image](https://github.com/Nicolas-Hinestroza/Reto-11_UNAL/assets/124611099/20736b9a-dd9c-4aaa-a236-599d6af8f1c8)
![image](https://github.com/Nicolas-Hinestroza/Reto-11_UNAL/assets/124611099/1ff451e7-cd7b-4187-8866-e71632ea8cc7)

    #1. Desarrolle un programa que permita realizar la suma/resta de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.

    def ingresar_matriz():
        filas = int(input("Escribe el número de filas de la matriz: "))
        columnas = int(input("Escribe el número de columnas de la matriz: "))
        matriz = []   
        for i in range(filas):
            fila = []
            for j in range(columnas):
                elemento = int(input(f"Escribe el elemento en la posición [{i}][{j}]: "))
                fila.append(elemento)
            matriz.append(fila)   
        return matriz

    def suma_matrices(matriz1, matriz2):
        filas = len(matriz1)
        columnas = len(matriz1[0])
        if filas != len(matriz2) or columnas != len(matriz2[0]):
            return None
        resultado = []
        for i in range(filas):
            fila = []
            for j in range(columnas):
                suma = matriz1[i][j] + matriz2[i][j]
                fila.append(suma)
            resultado.append(fila)
        return resultado

    def resta_matrices(matriz1, matriz2):
        filas = len(matriz1)
        columnas = len(matriz1[0])
        if filas != len(matriz2) or columnas != len(matriz2[0]):
            return None
        resultado = []
        for i in range(filas):
            fila = []
            for j in range(columnas):
                resta = matriz1[i][j] - matriz2[i][j]
                fila.append(resta)
            resultado.append(fila)
        return resultado

    print("Ingrese la primera matriz:")
    matriz1 = ingresar_matriz()
    print("Ingrese la segunda matriz:")
    matriz2 = ingresar_matriz()
    print("\nMatriz 1:")
    for fila in matriz1:
        print(fila)
    print("\nMatriz 2:")
    for fila in matriz2:
        print(fila)
    resultado_suma = suma_matrices(matriz1, matriz2)
    if resultado_suma is not None:
        print("\nSuma de matrices:")
        for fila in resultado_suma:
            print(fila)
    else:
        print("No se pueden sumar las matrices debido a dimensiones incorrectas.")
    resultado_resta = resta_matrices(matriz1, matriz2)
    if resultado_resta is not None:
        print("\nResta de matrices:")
        for fila in resultado_resta:
            print(fila)
    else:
        print("No se pueden restar las matrices debido a dimensiones incorrectas.")

- **2. Desarrolle un programa que permita realizar el producto de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.**

![image](https://github.com/Nicolas-Hinestroza/Reto-11_UNAL/assets/124611099/fe95f457-a21a-4604-864f-e66b22641385)

    #2. Desarrolle un programa que permita realizar el producto de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.

    def ingresar_matriz(filas, columnas): 
         matriz = []
         for i in range(filas):
            fila = []
            for j in range(columnas):
                elemento = int(input(f"Ingrese el elemento [{i}][{j}]: "))
                fila.append(elemento)
            matriz.append(fila)
         return matriz

    def multiplicar_matrices(matriz1, matriz2):
        resultado = [] 
        for i in range(len(matriz1)):
            fila = []
            for j in range(len(matriz2[0])): 
                elemento = 0 
                for k in range(len(matriz2)):
                    elemento += matriz1[i][k] * matriz2[k][j] 
                fila.append(elemento)
            resultado.append(fila) 
        return resultado

    if __name__ == "__main__":
     filas = int(input("Ingrese el número de filas de las matrices: "))
     columnas = int(input("Ingrese el número de columnas de las matrices: "))
     matriz1 = ingresar_matriz(filas, columnas)
     print("matriz 1:", matriz1)
     matriz2 = ingresar_matriz(filas, columnas)
     print("Matriz 2",matriz2)
    if len(matriz1) != len(matriz2) or len(matriz1[0]) != len(matriz2[0]):
        print("Error: Las matrices deben tener las mismas dimensiones para realizar la operación.")
    else:
        matriz_multiplicacion = multiplicar_matrices(matriz1, matriz2)
        print("el producto de las matrices es:")
        for fila in matriz_multiplicacion:
            print(fila)

- **3. Desarrolle un programa que permita obtener la matriz transpuesta de una matriz ingresada. El programa debe validar las condiciones necesarias para ejecutar la
operación.**

![image](https://github.com/Nicolas-Hinestroza/Reto-11_UNAL/assets/124611099/2c1e18ec-5c45-4030-8665-c4ba1c42f4dc)

    #3. Desarrolle un programa que permita obtener la matriz transpuesta de una matriz ingresada. El programa debe validar las condiciones necesarias para ejecutar la operación.

    def ingresar_matriz(filas, columnas):
        matriz = []
        print("Ingrese los elementos de la matriz:")
        for i in range(filas):
            fila = []
            for j in range(columnas):
                elemento = int(input(f"Ingrese el elemento en la posición [{i}][{j}]: "))
                fila.append(elemento)
            matriz.append(fila)
        return matriz
 
    def matriz_transpuesta(matriz):
        filas = len(matriz)
        columnas = len(matriz[0])
        matriz_transpuesta = []
        for j in range(columnas):
            fila = []
            for i in range(filas):
                fila.append(matriz[i][j])
            matriz_transpuesta.append(fila)
        return matriz_transpuesta

    filas = int(input("Ingrese el número de filas de la matriz: "))
    columnas = int(input("Ingrese el número de columnas de la matriz: "))
    matriz = ingresar_matriz(filas, columnas)
    print("\nMatriz ingresada:")
    for fila in matriz:
        print(fila)
    matriz_transpuesta = matriz_transpuesta(matriz)
    print("\nMatriz transpuesta:")
    for fila in matriz_transpuesta:
        print(fila)

- **4. Desarrollar un programa que sume los elementos de una columna dada de una matriz.**

![image](https://github.com/Nicolas-Hinestroza/Reto-11_UNAL/assets/124611099/29473c04-6cde-4ae9-9cfc-f0d5ff644326)

    #4. Desarrollar un programa que sume los elementos de una columna dada de una matriz.

    def ingresar_matriz(filas, columnas): 
         matriz = [] 
         for i in range(filas):
            fila = [] 
            for j in range(columnas):
                elemento = int(input(f"Ingrese el elemento [{i}][{j}]: "))
                fila.append(elemento) 
            matriz.append(fila)
         return matriz

    def sumar_columna(matriz, columna):
        suma = 0
        for i in range(len(matriz)):
            suma += matriz[i][columna]  
        return suma

    if __name__ == "__main__":
     filas = int(input("Ingrese el número de filas de la matriz: "))
     columnas = int(input("Ingrese el número de columnas de la matriz: "))
     matriz = ingresar_matriz(filas, columnas)
     for fila in matriz:
      print (fila)
     columna = int(input("Ingrese el número de columna a sumar: "))
     suma_columna = sumar_columna(matriz, columna)
     print(f"La suma de la columna {columna} es: {suma_columna}")

- **5. Desarrollar un programa que sume los elementos de una fila dada de una matriz.**

![image](https://github.com/Nicolas-Hinestroza/Reto-11_UNAL/assets/124611099/05a8e326-dc09-4430-a969-ae72931836c7)

    A = [[1, 4, 9], [16, 25, 36], [49, 64, 81]] # Definimos la matriz
    b = 0 # Definimos la variable b igual a 0
    for i in range(len(A)): # Recorre filas
        suma = 0 # Definimos suma = 0 para que el valor se reinicie 
        b = b + 1 # esta es la variable para enumerar las filas
        for j in range(len(A[i])): # Recorre cada elemento de la fila
           suma = suma + A[i][j] # Suma es igual a la suma de todos los valores de la fila
        print("La suma de la fila #" + str(b) + " es igual a ", suma) # Imprimimos el resultado

