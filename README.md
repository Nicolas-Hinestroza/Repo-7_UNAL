# Repo-7_UNAL
Para cada punto se debe crear un programa individual cada punto debe tener su respectiva explicación

- **1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.**

![image](https://user-images.githubusercontent.com/124611099/228120375-7ab69bf4-999a-494e-aa8e-aaadfd2aebf9.png)

    # PUNTO NUMERO 1
    n = 0 # Definimos la variable n
    while n < 100: # Mientras que n sea menor que 100 haga
    n += 1 # n es igual al valor mas 1 y asi se repite
    print("Este es el valor " + str(n) + " y su cuadrado es: " + str(n**2)) # Cuando el proceso llega a su fin imprimimos
 
- **2. Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.**

![image](https://user-images.githubusercontent.com/124611099/228121239-0d5779d3-fd49-40b3-a8b9-b744965d3b18.png)

    # PUNTO NUMERO 2
    p : int = 0 # Asignamos p para definir las variables pares
    i : int = 0 # Asignamos i para definir las variables impares
    i = 2 * n + 1 # se define una formula sensilla para sacar los numeros impares
    while (p < 1000): # Mientras que p sea menor que mil haga:
           p += 1  # p se le supa uno para que quede valiendo 1
       if p % 2 != 0: # Ahora este proceso va a hacer que se impriman todos los numeros pares
          continue
       print("los valores pares son: " + str(p) + " y los valores impares son: " + str(i)) # Se imprimen los resultados 
    i += 2  # Ahora este proceso va a hacer que se impriman todos los numeros impares

- **3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado.**

![image](https://user-images.githubusercontent.com/124611099/228125658-d0fed273-554c-48e6-996d-9ac095c024fc.png)

    # PUNTO NUMERO 3
    n = int(input("Escribe un valor mayor que 2: ")) # se define la variable n 
    while n < 2: # debe ser un numero mayor que 2
       n = int(input("ERROR, Digita un valor mayor que 2")) # si no es asi se imprime error.
    while n >= 2: # Mientras que n sea mayor o igual a 2 haga
       if n % 2 == 0: # si el residuo de la division entre n y 2 es de 0 asi solo imprimiremos los pares 
          print("Este es el valor numero " + str(n)) # Se imprimen los numeros
    n -=2 # Utilizamos esta operacion para que n vaya disminuyendo de 2 en 2

- **4. En 2022 el país A tendrá una población de 25 millones de habitantes y el país B de 18:9 millones. Las tasas de crecimiento anual de la población serán de 2% y 3% respectivamente. Desarrollar un algoritmo para informar en que año la población del país B superará a la de A.**

![image](https://user-images.githubusercontent.com/124611099/228126297-9a0d83c6-0757-44ff-a8c3-c4c3a0ae623f.png)

    # PUNTO NUMERO 4
    A = 25000000 # Definimos la variable A como el pais A
    B = 18900000 # Definimos la variable B como el pais B
    Crecimiento_A = 0.02 # Definimos la tasa de crecimiento del pais A
    Crecimiento_B = 0.03 # Definimos la tasa de crecimiento del pais B
    Temporada = 2022 # Definimos el año 
    while B < A: # Mientras que el pais B sea menor que A haga
        Temporada += 1 #Se le va sumando un año segun la taza de crecimiento de los paises
        A += A * Crecimiento_A # utilizamos una operacion en la que A es el valor de la poblacion por la taza de crecimiento del pais A
        B += B * Crecimiento_B # utilizamos una operacion en la que B es el valor de la poblacion por la taza de crecimiento de pais B
    print("El Pais B supero a el Pais A en el año " + str(Temporada)) #Imprimimos el resultado de los procesos
        
- **5. Imprimir el factorial de un número natural n dado.**

![image](https://user-images.githubusercontent.com/124611099/228126892-0f339600-6d57-42c1-9846-9d2c4ba39c16.png)

    # PUNTO NUMERO 5
    n = int(input("Escribe un valor: ")) # Primero vamos a definir n como la variable que el programa va a leer
    f = 1 # f la variable para definir a los factoriales
    m = n # m va a ser el mismo n solo que lo vamos a utilizar para la impresion de resto es innecesario 
    while n > 0: # mientras que n sea mayor que 0 haga
        f*= n # f es el valor que quedara valiendo despues de multiplicarse entre f y n
        n -= 1 # para que se cumpla la relacion de los factoriales n debe de ir bajando hasta llegar a 0
    print("El factorial del valor " + str(m) + " es: " + str(f)) # cuando se complete el proceso se imprimira el numero digitado (n) y el factorial (f)

- **6. Implementar un algoritmo que permita adivinar un número dado de 1 a 100, preguntando en cada caso si el número es mayor, menor o igual.**

![image](https://user-images.githubusercontent.com/124611099/228129633-d8c59894-5f6a-43e2-bb16-a0bb8e9309df.png)

    m : int = 1 # vamos a definir la variable M como el tope maximo para que el programa adivine
    M : int = 100 # vamos a definir la variable m como el tope minimo para que el programa adivine
    n : bool = False # se define como un bool si es falso se acaba el programa
    l = input(" Hola, piensa en un numero y yo lo voy a adivinar ¿Estas listo? (si/no)") # Colocamos este comentario para que el programa se vea mas bonito :)
    if l.lower() == "si": # si deice que si el programa continua
         while not n: # Mientras no sea n haga
               i = (M + m) // 2 # vamos a dar un inicio al programa asi este evidenciara si necesita aumentar o disminuir.
               r = input("¿El numero en el que estabas pensando es " + str(i) +"? (si/no)") # aca preguntamos si el numero i (es decir el inicio) es el numero en el que pensaba
               if r.lower() == "si": # si el numero es el que pensaba...
                  n = True # el programa llega a su fin y a adivinado el numero
                  print("Lo logre ya adivine tu valor y es " + str(i) + ", ten un lindo dia ;)") # imprime que a adivinado el numero e imprime el numero
               elif r.lower() == "no": # si el numero i no es entonces el programa preguntara...
                  r = input("El numero es mayor o menor que " + str(i) + "? (mayor/menor)") # el programa preguntara si es mayor o menor que i 
               if r.lower() == "mayor": # si es mayor el programa...
                  m = i + 1 # El programa realizara una operacion en el cual el tope minimo es igual a i (el valor con el que veniamos) y le sumara 1
               elif r.lower()=="menor": # si es menor el programa...
                  M = i - 1 # El programa realizara una operacion en el cual el tope maximo es igual a i (el valor con el que veniamos) y le sumara 1
              # Todo este proceso se va a ir repitiendo y el programa se va a ir preguntando segun lo que tu contestes hasta que se adivine el numero.
    else:
       print("Lo siento el valor que ingresaste no es valido :( ") # Si se escribe otro tipo de respuesta pues se imprimira error.

- **7. Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.** 

![image](https://user-images.githubusercontent.com/124611099/228135066-d2e06152-1471-47ed-9b45-35f7a8470dff.png)

    # PUNTO NUMERO 7
    n = int(input("Escribe un valor menor que 50 y mayor que 2: ")) # vamos a definir la variable n como el numero que recibe el programa
    a = 1 # a van a ser los divisores
    if n < 50 and n > 2: # Primero para confirmar que el numero digitado sea 2 < n < 50...
       print ("Los divisores de " + str(n) + " son ") # imprimimos para que el programa se vea mas bonito.
       while a <= n: # Mientras que a sea menor o igual que n haga
           if n % a == 0: # si el residuo de la division enytre a y n es 0 entonces...
             print (a) # imprimir los divisores. 
           a += 1 # para ir mirando se van sumando los numeros esperando que se encuentre algun divisor.
    else:
       print("ERROR, Diguita un valor que sea menor que 50 y mayor que 2") # si el numero digitado no se encuentra dentro del rango solicitado escribir error.


- **8. Implementar el algoritmo que muestre los números primos del 1 al 100. nota: use funciones**

