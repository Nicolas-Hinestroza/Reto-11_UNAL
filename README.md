# Reto-11_UNAL
Desarrolle la mayoría de ejercicios en clase, por cado punto resuelto en clase tendrá media décima en el examen 2 (creanme, las van a necesitar). Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_11 en slack.

- **1. Desarrolle un programa que permita realizar la suma/resta de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.**

- **2. Desarrolle un programa que permita realizar el producto de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.**

- **3. Desarrolle un programa que permita obtener la matriz transpuesta de una matriz ingresada. El programa debe validar las condiciones necesarias para ejecutar la
operación.**

- **4. Desarrollar un programa que sume los elementos de una columna dada de una matriz.**

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

