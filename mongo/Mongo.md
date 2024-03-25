Estructura de un JSON:
```
{
  "clave1": "valor1",
  "clave2": "valor2",
  "clave3": {
    "clave3-1": "valor3-1",
    "clave3-2": "valor3-2"
  },
  "clave4": ["valor4-1", "valor4-2", "valor4-3"]
}
```

# Explicación de la estructura JSON anterior:
- Cada conjunto de datos "clave: valor" está separado por una coma (,).
- Las claves son representadas como strings y están encerradas entre comillas dobles (").
- Los valores pueden ser strings, números, booleanos, arrays (listas) u otros objetos JSON.
- Los arrays son indicados con corchetes ([]) y pueden contener datos de cualquier tipo, incluyendo otros arrays u objetos JSON.
- Los objetos JSON se presentan con llaves ({}) y contienen pares de "clave: valor".
- Este ejemplo proporciona una visión básica; los JSON pueden ser considerablemente más complejos según los datos que se deseen almacenar.

Para agrupar múltiples documentos en una sola colección:

En el siguiente ejemplo, cada objeto dentro del array (los corchetes) representa un documento que podría ser insertado en una colección de una base de datos, por ejemplo. Cada documento posee sus propias claves y valores que representan los campos y sus respectivos valores.
```
[
  {
    "Categoria1": "John",
    "apellido": "Doe",
    "edad": 30,
    "direccion": "123 Avenida Principal"
  },
  {
    "nombre": "Alice",
    "apellido": "Smith",
    "edad": 28,
    "direccion": "456 Calle Secundaria"
  },
  {
    "nombre": "Bob",
    "apellido": "Johnson",
    "edad": 32,
    "direccion": "789 Calle Terciaria"
  }
]
```

NOTA: En MongoDB, es necesario asignar un campo de identificación (-id), si no se proporciona, se generará automáticamente.

El siguiente ejemplo muestra cómo hacerlo:
```
[
  {
    "-id": 1,
    "nombre": "Linea Blanca",
    "Productos":{
      "nombre": "Refrigerador",
      "stock": 17
    } 
  },
  {
    "-id": 2,
    "nombre": "Lacteos",
    "Productos": [
      {
        "nombre": "Leche de burra fresca",
        "stock": 22
      },
      {
        "nombre": "Leche de burra fresca",
        "stock": 22
      }
    ]
  }
]