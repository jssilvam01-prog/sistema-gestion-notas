# Sistema de Gestión de Notas

Aplicación de consola en Python para gestionar estudiantes y sus calificaciones.

## Descripción

Este es un sistema de gestión académica que permite:
- Registrar estudiantes con nombre e ID
- Agregar notas (valores entre 0 y 5)
- Calcular el promedio de cada estudiante
- Mostrar reportes con estado (Aprobado/Reprobado)
- Persistir datos en archivo JSON

## Requisitos

- Python 3.x (no requiere librerías externas)
- Solo usa la biblioteca estándar de Python

## Cómo ejecutar

```bash
python main.py
```

## Funcionalidades

### 1. Registrar estudiante
Permite registrar un nuevo estudiante con:
- ID único (no puede repetirse)
- Nombre del estudiante

### 2. Agregar nota
Agrega una nota a un estudiante existente:
- Valida que la nota esté entre 0 y 5
- Múltiples notas por estudiante

### 3. Mostrar reporte
Muestra una tabla con:
- ID del estudiante
- Nombre
- Promedio (redondeado a 2 decimales)
- Estado (Aprobado si promedio >= 3.0)

### 4. Guardar datos
Guarda todos los datos en el archivo `notas.json` para persistencia.

### 5. Salir
Pregunta si desea guardar antes de cerrar el programa.

## Estructura del código

- `cargar_datos()`: Carga datos desde JSON
- `guardar_datos()`: Guarda datos en JSON
- `registrar_estudiante()`: Registra nuevo estudiante
- `agregar_nota()`: Agrega nota a estudiante
- `calcular_promedio()`: Calcula promedio
- `mostrar_reporte()`: Muestra reporte completo
- `mostrar_menu()`: Muestra opciones del menú
- `main()`: Función principal

## Archivo de datos

Los datos se guardan en `notas.json` con el siguiente formato:

```json
{
    "ID001": {
        "nombre": "Juan Perez",
        "notas": [4.5, 3.8, 4.2]
    }
}
```

## Licencia

Este proyecto es de uso libre para fines educativos.
