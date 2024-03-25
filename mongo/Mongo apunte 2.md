
# inserción de un documento con subdocumentos, y con el id personalizado:

```javascript
fabricantes> db.fabricantes.insertOne({
"_id": 1,
"nombre": "fab1",
"Localidad": {
"Ciudad": "Buenos Aires",
"Pais": "Argentina",
"Calle": "Calle Pez 27"
"Cod": 29000
}
...
})
{ acknowledged: true, insertedId: 1}
fabricantes> |
```
# Para ver todos los documentos de una colección, se utiliza db.nombreDeLaColeccion.find() (Es como el select en SQL):
```
db1> db.empleados.find()
[
{_id: ObjectId('65c3bd710df8eb8e1890435f'), nombre: 'Jose Angel' },
{
_id: ObjectId('65c3bf850df8eb8e18904360'),
nombre: 'Benjamin',
apellido: 'Peña',
edad: 40
}
]
db1> |

```
# Para eliminar una base de datos, se utiliza db.dropDatabase('nombreDeLaDataBase'). No es necesario estar ubicado en la base de datos que vamos a eliminar.

.	db.dropDatabase(‘nombreDeLaDataBase’) Sirve para eliminar una base de datos. No hay que estar ubicados en la BD que vamor a eliminar.

db.nombreDeLaColeccion.insertMany([{  }]) Sirve para insertar varios documentos a la vez pero dentro de un arreglo, adentro del ([{ van los documentos.

Para insertar varios documentos a la vez pero dentro de un arreglo, se utiliza db.nombreDeLaColeccion.insertMany([]) donde dentro de los corchetes van los documentos a insertar.
```
Ejemplo:
db.nombreDeLaColeccion.insertMany([
  { documento1 },
  { documento2 },
  { documento3 }
])


```
```javascript
db1> db.empleados.insertMany(
[
{
nombre: "Hermenegildo",
edad: 67
},
{
nombre: "Soy la la vaaca del corral",
edad: 14,
sexo: "Mujer"
},
{
nombre: "Romulo",
edad: 40,
nacionalidad: "Nigeriano"
},
{
nombre: "Cristian Andres",
localidad: "San Miguel de las Piedras",
nacionalidad: "Aleman",
edad: "Esta morro"
}]
)
```
## Para hacer consultas con filtro en una colección, se utiliza db.nombreDeLaColeccion.find({filtro}).


```
 db1> db.libros.find({precio:25})
[
{
_id: 5,
titulo: 'Python para torpes',
editorial: 'Planeta',
precio: 25,
cantidad: 14
},
{
_id: 6,
titulo: 'Don quijote',
editorial: 'Biblio',
precio: 25,
cantidad: 14
},
{
_id: 9,
titulo: 'JSON para todos',
editorial: 'Planeta',
precio: 25,
cantidad: 15
}
]

db1> db.libros.find({precio:{$eq:25}})
```
#  	Podemos ver para ver los operadores de consulta en la documentacion: 


	En este ejemplo agarre un operador de contulta de la documentacion (lt que significa menor que) En esta consulta le digo traeme los documentos en donde cantidad sea menor a 5.

```

```
# Aquí hago otro ejemplo: Aquí le digo traeme todos los documentos de la colección libros en donde 
```db1> db.libros.find({editorial: {$in: ["Biblio", "Planeta")}})
{
_id: 1,
titulo: 'El aleph',
autor: 'Borges',
editorial: 'Planeta',
precio: 20,
},
{
cantidad: 50
_id: 5,
titulo: 'Python para torpes',
editorial: 'Planeta',
precio: 25,
cantidad: 14
},
_id: 6,
titulo: 'Don quijote',
editorial: 'Biblio',
precio: 25,
cantidad: 14
},
{
_id: 7,
titulo: 'MongoDB para expertos',
editorial: 'Biblio',
precio: 34,
cantidad: 29

```
# Si utilizo findOne solo me trae el primero que encuentre con la condicion que le pedi, por ejemplo aquí le digo: Traeme el primer documento que encuentres en la colección de libros donde precio sea 20 o 25.


```
db1> db.libros.findOne({precio: {$in: [20, 25]}})
{
_id: 1,
titulo: 'El aleph',
autor: 'Borges',
editorial: 'Planeta',
precio: 20,
cantidad: 50
}
db1> 
```
# Tambien hay consultas con and, su sintaxis es la del ejemplo: Traeme todos los documentos de la colección libros donde precio sea mayor a 25 AND cantidad menor a

```
db1> db.libros.find({precio: {$gt: 25}, cantidad: {$lt: 15}})
[
{
_id: 2,
titulo: 'Martin Fierro'
autor: Jose Hernandez'
editorial: 'Siglo XXI',
precio: 50,
},
{
}
]
cantidad: 12
_id: 4,
titulo: 'Java en 10 minutos',
editorial: 'Siglo XXI',
precio: 45, cantidad: 1
db1>

```
# Aquí hago lo mismo pero con diferente sintaxis, pero igual es una consulta con AND

```
db1> db.libros.find({$and: [{precio: {$gt:25}}, {cantidad: {$lt:15}}]})
[
{
_id: 2,
titulo: 'Martin Fierro'
autor: 'Jose Hernandez', editorial: 'Siglo XXI',
precio: 50,
cantidad: 12
},
{
}
]
_id: 4,
titulo: 'Java en 10 minutos',
editorial: 'Siglo XXI',
precio: 45,
cantidad: 1
db1>

```
#  En este ejemplo estamos haciendo una consulta con or, decimos que nos traiga todos los documentos de la colección libros

```
db1> db.libros.find({
$or: [{precio: {$gt:25}},{cantidad: {$lt:15}}]})

```
#  Asi es para hacer una consulta en una colección solo mostrando un campo en este caso solo quiero que me muestre los titulos de los documentos:

```
[
db1> db.libros.find({}, {titulo:1})
{_id: 1, titulo: 'El aleph' },
{_id: 2, titulo: 'Martin Fierro' },
{_id: 3, titulo: 'Aprenda PHP' },
{_id: 4, titulo: 'Java en 10 minutos' },
{_id: 5, titulo: 'Python para torpes' },
{ id: 6, titulo: 'Don quijote' },
{ id: 7, titulo: 'MongoDB para expertos' },
{ id: 8, titulo: 'MongoDB para novatos' },
{ id: 9, titulo: 'JSON para todos' }
]
db1> |

```
# Si por ejemplo quiero mostrar solo ciertos campos y que no me muestre el id, la sintaxis es la siguiente:. Aquí le digo que me traiga los documentos de la colección libros en donde el titulo exista.

```
db1> db.libros.find({titulo: {$exists:true}})


```
#  Aquí le digo que me traiga los documentos de la colección libros en donde el dato del campo precio sea de tipo double.

```
db1> db.libros.find({precio: {$type: 'double'}})
[
{
_id: 12,
titulo: 'Estupro',
fianza: true,
anios_carcel: 'dos',
precio: 13.45
}
]
db1> |
```
#  Update, actualizaciones de un documento: Primero hago la consulta del documento con id 9, en la colección libros.

```
db1> db.libros.find({_id:9})
[
{
_id: 9,
titulo: 'JSON para todos',
editorial: 'Planeta',
precio: 25,
cantidad: 15
}
]


```
# Ahora Hago la actualizacion: en donde en titulo tenga JSON para todos, y ahora dira Java el rey.

```
db1> db.libros.updateOne({ titulo: JSON para todos' }, { $set: { titulo: 'Java el rey' } })
{
acknowledged: true,
insertedId: null,
matchedCount: 1,
modifiedCount: 1,
upsertedCount: 8


```
# Si consulto de nuevo, ya se hicieron los cambios:

```
db1> db.libros.find({_id:9})
[
{
_id: 9,
titulo: 'Java el rey',
editorial: 'Planeta',
precio: 25,
}
cantidad: 15
]
db1>

```
