#CREAR MATRIZ DE HORAS DE TRABAJO#
matriz_horas=[
    ["Maria", 8, 9, 8, 9, 8],
    ["Juan", 7, 8, 6, 9, 7],
    ["Ana", 8, 9, 8, 9, 7],
    ["Pedro", 8, 8, 8, 8, 8]
]
#CALCULAR EL TOTAL DE HORAS TRABAJADAS POR CADA EMPLEADO#
def procesar_jornada(fila_recuso):
    nombre_empleado = fila_recuso[0]
#SUMAR LAS HORAS TRABAJADAS#
    horas_trabajadas = sum(fila_recuso[1:])
#CLASIFICAR LA JORNADA LABORAL#
    if horas_trabajadas >40:
        clasificacion = "Sobretiempo"
    else:
        clasificacion = "Horario Estandar"
#RETORNAR LOS RESULTADOS#
    return (nombre_empleado, horas_trabajadas, clasificacion)
#IMPRIMIR LOS RESULTADOS#
print ("Resultados de la jornada laboral de los empleados:")
print("---------------------------------------------")
for fila in matriz_horas:
    nombre, horas, clasif = procesar_jornada(fila)
    print(f"{nombre}: {horas} horas - {clasif}")
print("---------------------------------------------")
