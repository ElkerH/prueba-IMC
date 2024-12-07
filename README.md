# prueba-IMC
# Generación de código para ingresar datos sobre la persona y dar su Índice de Masa Corporal con indicación en que situación del IMC se encuentra de salud

nombre = input("introduce tu nombre:") #se le pide el nombre al usuario
apellidopaterno = input("introduce tu apellido paterno:") #se registra su apellido paterno y maaterno
apellidomaterno = input("introduce tu apellido materno:")
edad = int(input("introduce tu edad: ")) #se introduce su edad y se le pone la funcion -int- para validacion de que son numeros enteros

# Se realiza una lista donde nos vasaremos los datos que tomaremos en cuenta para validar los datos de IMC para el usuario 
""" niveles de clasificacion de IMC
    IMC       Clasificacion
-----------------------------
< 18.5        ->Bajopeso
18.5 - 24.9   ->Normal
25.0 - 29-9   ->Sobrepeso
30.0 - 34.9   ->Obesidad I
35.0 - 39.9   ->Obesidad II
40.0 - 49.9   ->Obesidad III
    >50       ->Obesidad IV """
    # se ingrea def para tomar en cuenta la lsita siguiente
def niveldepeso(IMC):
    if IMC <18.5:
        return "Bajopeso:" # si la respuesta es menor al 18.5 seria que la persona tiene bajo peso
    elif 18.5 <= IMC <=24.9:
        return "Normal"
    elif 25.0 <= IMC <=29.9:
        return "Sobrepeso"
    elif 30.0 <= IMC <=34.9:
        return "Obesidad I"
    elif 35.0 <= IMC <=39.9:
        return "Obesidad II"
    elif 40.0 <= IMC <=49.9:
        return "Obesidad III"
    elif IMC <=50:
        return"Obesidad IV"  

peso = float(input("introduce tu peso en Kg: ")) #siguiendo con el peso de la persona, se le coloca la funcion -float- ya que lleva como el peso y la estatura pueden llevar punto decimal y numeros enteros
estatura = float(input("ingresa tu altura en m: "))
imc = peso /pow(estatura,2) #se coloca la funcion -pow- para mejorar la funcion de exponentes
imc = round(imc,2) #se hace un redodndeo con la funcio- round- para que solo se muestre el IMC con dos decimales 

print("Nombre:" + nombre)
print("Apellido-Paterno:" + apellidopaterno)
print("Apellido-Materno:" + apellidomaterno)
print("Edad:" + str(edad) + "años")
print("Su nivel de peso es:",niveldepeso(imc))
