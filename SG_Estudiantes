#Se crean las listas para almacenar los datos
identificaciones = []
nombres = []
edades = []
programas = []
nota1 = []
nota2 = []
nota3 = []
promedios = []
resultados = []

#Función para agregar estudiantes
def agregar_estudiante():
    print("\n*** AGREGAR ESTUDIANTE ***")
    identificacion = input("Ingrese el ID del estudiante: ")
    #Se valida que la identificación no esté vacía
    if identificacion == "":
        print("Error: debe ingresar un número de identificación")
    else:
        #Se crea una variable bandera para comprobar si la identificación ya existe
        existe = False
        # Se recorre la lista para verificar si el ID está repetido
        for i in range(len(identificaciones)):
            if identificaciones[i] == identificacion:
                existe = True
        # Si existe la identificación, no se permite repetirla.
        if existe == True:
            print("Error: el ID ya se encuentra registrado")
        else:
            nombre = input("Ingrese el nombre del estudiante: ")
            if nombre == "":
                print("Error: el campo no puede estar vacío")
            else:
                # while True permite volver a solicitar la edad cuando el usuario ingresa un dato incorrecto
                while True:
                    try:
                        edad = int(input("Ingrese la edad del estudiante: "))
                        if edad >= 14:
                            if edad <= 100:
                                break
                            else:
                                print("Error: la edad no puede superar los 100 años")
                        else:
                            print("Error: la edad debe ser mayor o igual a 14")

                    except ValueError:
                        print("Error: debe ingresar una edad utilizando números enteros")

                # Se solicita el programa académico
                programa = input("Ingrese el programa académico: ")
                if programa == "":
                    print("Error: el programa académico no puede estar vacío")
                else:
                    #Se ingresan y se validan las 3 notas - Primera nota
                    while True:
                        try:
                            nota_1 = float(input("Ingrese la primera nota (0.0 - 5.0): "))
                            if nota_1 >= 0.0:
                                if nota_1 <= 5.0:
                                    break
                                else:
                                    print("Error: la nota no puede ser superior a 5.0.")
                            else:
                                print("Error: la nota no puede ser inferior a 0.0.")

                        except ValueError:
                            print("Error: debe ingresar una nota numérica.")

                    #Segunda nota
                    while True:
                        try:
                            nota_2 = float(input("Ingrese la segunda nota (0.0 - 5.0): "))
                            if nota_2 >= 0.0:
                                if nota_2 <= 5.0:
                                    break
                                else:
                                    print("Error: la nota no puede ser superior a 5.0.")
                            else:
                                print("Error: la nota no puede ser inferior a 0.0.")

                        except ValueError:
                            print("Error: debe ingresar una nota numérica.")

                    #Tercera nota
                    while True:
                        try:
                            nota_3 = float(input("Ingrese la tercera nota (0.0 - 5.0): "))
                            if nota_3 >= 0.0:
                                if nota_3 <= 5.0:
                                    break
                                else:
                                    print("Error: la nota no puede ser superior a 5.0")
                            else:
                                print("Error: la nota no puede ser inferior a 0.0")

                        except ValueError:
                            print("Error: debe ingresar una nota numérica.")

                    #Cálculo promedio, la variable "sumatoria" acumula las tres notas
                    sumatoria = nota_1 + nota_2 + nota_3
                    promedio = sumatoria / 3

                    if promedio >= 3.0:
                        resultado = "APROBÓ"
                    else:
                        resultado = "REPROBÓ"

                    # Se almacenan los datos en las listas
                    identificaciones.append(identificacion)
                    nombres.append(nombre)
                    edades.append(edad)
                    programas.append(programa)
                    nota1.append(nota_1)
                    nota2.append(nota_2)
                    nota3.append(nota_3)
                    promedios.append(promedio)
                    resultados.append(resultado)

                    print("\nEl estudiante ha sido registrado correctamente")
                    print("Promedio: ", promedio)
                    print("Resultado: ", resultado)


#Función para mostrar los estudiantes
def mostrar_estudiantes():
    print("\n*** LISTADO DE ESTUDIANTES ***")
    # Se comprube si existen estudiantes registrados
    if len(identificaciones) == 0:
        print("No hay estudiantes registrados")
    else:
        for i in range(len(identificaciones)):
            print("\nEstudiante número: ", i + 1)
            print("ID: ", identificaciones[i])
            print("Nombre: ", nombres[i])
            print("Edad: ", edades[i])
            print("Programa académico: ", programas[i])
            print("Primera nota: ", nota1[i])
            print("Segunda nota: ", nota2[i])
            print("Tercera nota: ", nota3[i])
            print("Promedio: ", promedios[i])
            print("Resultado académico: ", resultados[i])

#Función para buscar un esduainte por ID
def buscar_estudiante():
    print("\n--- BUSCAR ESTUDIANTE ---")
    identificacion = input("Ingrese el ID que desea buscar: ")
    encontrado = False

    # Se recorren todas las identificaciones
    for i in range(len(identificaciones)):
        if identificaciones[i] == identificacion:
            print("\nEstudiante encontrado")
            print("ID: ", identificaciones[i])
            print("Nombre: ", nombres[i])
            print("Edad: ", edades[i])
            print("Programa académico: ", programas[i])
            print("Primera nota: ", nota1[i])
            print("Segunda nota: ", nota2[i])
            print("Tercera nota: ", nota3[i])
            print("Promedio: ", promedios[i])
            print("Resultado académico:", resultados[i])

            # Se cambia el valor de la bandera
            encontrado = True
            # Se termina el ciclo porque se encuentra al estudiante
            break

    # Comprobamos si la búsqueda tuvo éxito.
    if encontrado == False:
        print("No se encontró ningún estudiante con ese ID")

#Función para mostrar los estudiantes en orden inverso
def mostrar_orden_inverso():
    print("\n*** ESTUDIANTES EN ORDEN INVERSO ***")

    if len(identificaciones) == 0:
        print("No hay estudiantes registrados")
    else:
        # Comenzamos en la última posición y avanzamos hacia la posición cero
        for i in range(len(identificaciones) - 1, -1, -1):
            print("\nEstudiante número: ", i + 1)
            print("ID: ", identificaciones[i])
            print("Nombre: ", nombres[i])
            print("Edad: ", edades[i])
            print("Programa académico: ", programas[i])
            print("Primera nota: ", nota1[i])
            print("Segunda nota: ", nota2[i])
            print("Tercera nota: ", nota3[i])
            print("Promedio: ", promedios[i])
            print("Resultado académico: ", resultados[i])

# Programa principal
# Variable bandera para controlar la salida del programa y variable de conteo para registrar la cantidad de estudiantes
salir = False
contador = 0

while salir == False:
    print("SISTEMA DE GESTIÓN DE ESTUDIANTES")
    print("======================================")
    print("(1) Agregar estudiante")
    print("(2) Mostrar estudiantes")
    print("(3) Buscar estudiante por ID")
    print("(4) Mostrar estudiantes en orden inverso")
    print("(5) Salir")

    try:
        opcion = int(input("Seleccione una opción (1-5): "))
    except ValueError:
        print("Error: debe ingresar una opción entre 1 a 5")
        continue

    match opcion:
        case 1:
            #Se guarda  la cantidad de estudiantes antes de ejecutar la función
            cantidad_anterior = len(identificaciones)
            agregar_estudiante()
            #Se comprueba cuántos estudiantes hay después
            cantidad_actual = len(identificaciones)

            # Si aumentó la cantidad, se actualiza el contador
            if cantidad_actual > cantidad_anterior:
                contador = contador + 1
            print("Total de estudiantes registrados: ", contador)

        case 2:
            mostrar_estudiantes()

        case 3:
            buscar_estudiante()

        case 4:
            mostrar_orden_inverso()

        case 5:
            print("\nGracias por utilizar el sistema")
            salir = True

        case _:
            print("\nOpción incorrecta. Seleccione una opción del 1 al 5")



