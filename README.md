# PROBLEMA-5-FASE-5-EVALUACION-POA
Desarollo de problemas mediante sistema de programación Python
# ==========================================
# CONTROL DE HORAS SEMANALES
# CON CANTIDAD VARIABLE DE EMPLEADOS
# ==========================================

# ---------- FUNCIÓN ----------
def calcular_horas(lunes, martes, miercoles, jueves, viernes):

total = lunes + martes + miercoles + jueves + viernes

if total > 40:
clasificacion = "Sobretiempo"
else:
clasificacion = "Horario Estándar"

return total, clasificacion


# ---------- PROCEDIMIENTO ----------
def mostrar_resultados(matriz):

print("\n===== REPORTE SEMANAL =====\n")

for recurso in matriz:

nombre = recurso[0]

lunes = recurso[1]
martes = recurso[2]
miercoles = recurso[3]
jueves = recurso[4]
viernes = recurso[5]

total, clasificacion = calcular_horas(
lunes,
martes,
miercoles,
jueves,
viernes
)

print("Empleado:", nombre)
print("Lunes:", lunes, "horas")
print("Martes:", martes, "horas")
print("Miércoles:", miercoles, "horas")
print("Jueves:", jueves, "horas")
print("Viernes:", viernes, "horas")
print("Total semanal:", total)
print("Clasificación:", clasificacion)
print("-" * 40)


# ---------- PROGRAMA PRINCIPAL ----------

matriz_recursos = []

# Solicitar cantidad de empleados
cantidad = int(input("Ingrese la cantidad de empleados: "))

# Estructura repetitiva para registrar empleados
for i in range(cantidad):

print("\nEmpleado", i + 1)

nombre = input("Nombre del empleado: ")

lunes = int(input("Horas trabajadas el lunes: "))
martes = int(input("Horas trabajadas el martes: "))
miercoles = int(input("Horas trabajadas el miércoles: "))
jueves = int(input("Horas trabajadas el jueves: "))
viernes = int(input("Horas trabajadas el viernes: "))

# Guardar datos en la matriz
matriz_recursos.append([
nombre,
lunes,
martes,
miercoles,
jueves,
viernes
])

# Mostrar resultados finales
mostrar_resultados(matriz_recursos)
