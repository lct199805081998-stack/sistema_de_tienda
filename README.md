💻 Documentación Técnica - Sistema de Tienda TechStore
🏪 Descripción General
El sistema TechStore es un programa interactivo que permite realizar búsquedas en una tienda de electrónica simulada.
Utiliza búsqueda lineal para encontrar productos y empleados según distintos criterios.
Está diseñado para funcionar fácilmente en Google Colab o entornos básicos de Python sin dependencias externas.

📦 Estructura de Datos
Productos
Cada producto es un diccionario con la siguiente estructura:

producto = {
    'id': int,
    'nombre': str,
    'marca': str,
    'categoria': str,
    'precio': float,
    'stock': int,
    'disponible': bool
}
Empleados
Cada empleado se representa así:

empleado = {
    'id': int,
    'nombre': str,
    'apellido': str,
    'departamento': str,
    'salario': float,
    'activo': bool
}
⚙️ Funcionalidades Principales
El programa permite:

Buscar productos por nombre, ID, categoría o marca.
Consultar productos disponibles en stock.
Buscar empleados por nombre completo, departamento o estado activo.
🧠 Descripción de Funciones
🔍 Búsqueda de Productos
Función	Descripción	Retorno
buscar_producto_por_nombre(productos, nombre)	Retorna los productos cuyo nombre contiene la cadena ingresada.	Lista de productos
buscar_producto_por_id(productos, id_producto)	Busca un producto por su identificador numérico.	Diccionario del producto o None
buscar_producto_por_categoria(productos, categoria)	Devuelve todos los productos de una categoría específica.	Lista de productos
buscar_productos_disponibles(productos)	Devuelve los productos con stock > 0.	Lista de productos
buscar_producto_por_marca(productos, marca)	Retorna productos de una marca determinada.	Lista de productos
👩‍💼 Búsqueda de Empleados
Función	Descripción	Retorno
buscar_empleado_por_nombre(empleados, nombre, apellido)	Busca un empleado por su nombre y apellido.	Diccionario o None
buscar_empleado_por_departamento(empleados, departamento)	Lista de empleados de un departamento.	Lista de empleados
buscar_empleados_activos(empleados)	Lista los empleados activos (activo=True).	Lista de empleados
🧩 Ejemplo de Ejecución
Al ejecutar el programa en Colab:

=== SISTEMA TECHSTORE ===
Opciones disponibles:
1. Buscar producto por nombre
2. Buscar producto por ID
3. Buscar producto por categoría
4. Buscar productos disponibles
5. Buscar producto por marca
6. Buscar empleado por nombre completo
7. Buscar empleado por departamento
8. Ver empleados activos
Seleccione una opción (1-8):
Ejemplo de búsqueda:

Ingrese el nombre del producto: iPhone 15
Resultado:
[{'id': 1, 'nombre': 'iPhone 15', 'marca': 'Apple', 'categoria': 'Smartphone', 'precio': 999.99, 'stock': 10, 'disponible': True}]
⏱️ Análisis de Complejidad
Todas las funciones utilizan búsqueda lineal, cuya complejidad temporal es:

[ T(n) = O(n) ]

donde n es el tamaño de la lista.
Esto significa que el tiempo de ejecución aumenta proporcionalmente al número de elementos.

Casos de eficiencia:
Es eficiente cuando la lista es pequeña o no está ordenada.
Si la lista crece demasiado, sería recomendable usar estructuras indexadas o búsqueda binaria.
⚠️ Manejo de Errores y Casos Especiales
Si no se encuentra un elemento, se retorna None o una lista vacía.
Las comparaciones no distinguen mayúsculas/minúsculas (.lower()).
Se permiten coincidencias parciales al buscar por nombre.
🚀 Mejoras Propuestas
Agregar persistencia de datos con archivos JSON.
Implementar búsqueda avanzada (por múltiples criterios).
Crear interfaz gráfica con tkinter.
Añadir historial de búsquedas y estadísticas.
🧾 Conclusiones
El sistema TechStore demuestra cómo la búsqueda lineal puede aplicarse efectivamente a estructuras de datos simples como listas de diccionarios.
Aunque no es el método más eficiente para grandes volúmenes, es ideal para entender el concepto de recorrido secuencial y su implementación práctica en Python.
