# ACTUALIZAR, ELIMINAR , CONSULTAR .......

# Si con el update queremos modificar un JSON que no tiene el campo que nosotros le dijimos que colocara, lo va a agregar como un nuevo campo:
En este caso agrego el campo de cantidad, antes no lo tenia, pero yo lo coloque en el update.

```
db1> db.libros.updateOne({ "_id": 11 }, { $set: { "precio": 10.2, "cantidad": 50 } }) {
acknowledged: true,
insertedId: null,
matchedCount: 1,
modifiedCount: 1,
upsertedCount: 0
}
db1> db.libros.find({_id:11})
[
{
_id: 11,
titulo: 'Los enamorados infieles',
autor: 'Benito Juarez',
precio: 10.2,
cantidad: 50
}
]
db1>


```
# Actualizar todos los documentos que encuentre: Quiero actualizar todos los documentos donde el precio sea mayor a 9, lo vamos a actualizar para que precio sea igual a 150 en todos esos documentos.

```
db1> db.libros.updateMany( { precio: { $gt: 9 } }, { $set: { precio: 150 } })
{
acknowledged: true, insertedId: null,
matchedCount: 12,
modifiedCount: 12,
upsertedCount: 0
}
db1>

```
# Ahora si observamos se modificaron varios documentos a 150
```
db1> db.libros.find({})
[
{
_id: 1,
titulo: 'El aleph',
autor: 'Borges',
editorial: 'Planeta',
precio: 150,
cantidad: 50
},
{
_id: 2,
titulo: 'Martin Fierro'
autor: Jose Hernandez',
editorial: 'Siglo XXI',
precio: 150,
cantidad: 12
},
{
_id: 3,
titulo: 'Aprenda PHP',
autor: Mario Molina'
editorial: 'Siglo XXI,
precio: 150,
cantidad: 20
},

```
# Ahora ocupamos updateMany para decir que en la colección libros quiero que le aumentes a todos los documentos en su precio 5, Sinc incrementa el valor de un campo. Si el precio era 150 y le incrementa 5, ahora el precio se actualizo a 155.

```
db1> db.libros.updateMany ( {}, {$inc: {precio:5}})
{
acknowledged: true,
insertedId: null,
matchedCount: 12, modified Count: 12,
upsertedCount: 0
}
db1>
```
#  Multiplicar el precio por 2 de las cantidades mayores a Aquí con Smul que sirve para multiplicar el valor de un campo. Entonces decimos que en en la colección libros, multiplique por 2 el precio que tengan los documentos que en cantidad tengan un valor mayor a 20.

```
db1> db.libros.updateMany( { cantidad: { $gt: 20 } }, { $mul: { precio: 2 } })
{
acknowledged: true,
insertedId: null,
matchedCount: 4,
modifiedCount: 4,
upsertedCount: 0
}
db1>


```
# El updateOne y el updateMany cambia los valores de los cambios o agrega un campo que no existe, pero con el replaceOne cambias los campos existentes en un documento, por ejemplo aquí solo dejo titulo cuando antes tenia mas campos.

```
db1> db.libros.replaceOne(
{
{"_id":10},{"titulo": "Las patoaventuras de Ezequiel alias Matteo"})
acknowledged: true,
insertedId: null,
matchedCount: 1,
modifiedCount: 1,
upsertedCount: 0
}
db1> db.libros.find({_id:10})
[ { id: 10, titulo: 'Las patoaventuras de Ezequiel alias Matteo' }]
db1>

```
# Eliminar Documentos (los datos) del campo. Para eso es deleteOne para uno en especifico en este caso con id 10, y si consulto el documento con id 10, ya no se ve nada porque esta eliminado.

```
db1> db.libros.deleteOne( {"_id":10})
{ acknowledged: true, deletedCount: 1}
db1> db.libros.find({_id:10})
db1>
```
# Y eso es para eliminar muchos campos con el deleteMany. Aquí le digo que elimine los registros o documentos en donde cantidad sea mayor a 20 y al dar enter me doy cuenta de que elimino 3 registros.

```
db1> db.libros.deleteMany( { cantidad: {$gt:20} })
{ acknowledged: true, deletedCount: 3}
db1> |

```
# Expresiones Regulares. Aquí digo: Buscar todos los titulos que contengan una t minuscula, hay que ser especifico con mayusculas y minusculas

```
db1> db.libros.find({"titulo":/t/})
[
{
_id: 2,
titulo: 'Martin Fierro
autor: Jose Hernandez', editorial: 'Siglo XXI',
precio: 155,
cantidad: 12
} },
},
_id: 4,
titulo: Java en 10 minutos',
editorial: 'Siglo XXI',
precio: 155,
cantidad: 1
{
_id: 5,
titulo: 'Python para torpes',
editorial: Planeta',
precio: 155,
cantidad: 14
},

```
# Traeme todos aquellos en donde en titulo terminen con "tos". Para eso se ocupa el signo de pesos $

```
db1> db.libros.find({"titulo":/tos$/})
[
{
_id: 4,
titulo: 'Java en 10 minutos',
editorial: 'Siglo XXI',
precio: 155,
cantidad: 1
},
{
_id: 8,
titulo: 'MongoDB para novatos'
editorial: 'Biblio',
precio: 155,
cantidad: 12
}
]
db1>

```
# Traeme todos los documentos en donde en el titulo, su nombre comience con M mayuscula, para eso se ocupa (se pone con Altgr + la tecla con su simbolo, se ocupa poner despues una letra para que salga)

```
db1> db.libros.find({"titulo":/^M/})
[
{
_id: 2,
titulo: 'Martin Fierro',
autor: Jose Hernandez',
editorial: 'Siglo XXI',
precio: 155,
},
cantidad: 12
لها {
_id: 8,
titulo: 'MongoDB para novatos',
editorial: 'Biblio',
precio: 155,
}
cantidad: 12
]
db1>
```
# Traeme todos los documentos que en su nombre tengan la palabra para, para eso se ocupa $regex

```
db1> db.libros.find({"titulo": {$regex:/para/}})
[
{
_id: 5,
titulo: 'Python para torpes',
editorial: Planeta',
precio: 155,
cantidad: 14
},
{
_id: 8,
titulo: 'MongoDB para novatos',
editorial: 'Biblio',
precio: 155,
cantidad: 12
}
]
db1> |

```
# Aquí le digo, traeme los documentos en donde titulo tengan la parabra MONGO sin importar mayuscular o minusculas, para eso le agregue options: i

```
[
db1> db.libros.find({"titulo": {$regex:/MONGO/, $options:"i"}})
{
_id: 8,
titulo: 'MongoDB para novatos',
editorial: 'Biblio',
precio: 155,
cantidad: 12
}
]
db1>
```
# Ordenar documentos: Seleccionar todos los documentos de libros pero solo

```
[
mostrando el titulo y el precio.
db1> db.libros.find({}, {titulo:1, precio:1, _id:0})
{titulo: 'Martin Fierro', precio: 155}, { titulo: 'Aprenda PHP', precio: 155},
{titulo: 'Java en 10 minutos', precio: 155},
{titulo: 'Python para torpes', precio: 155},
{titulo: 'Don quijote', precio: 155},
{titulo: 'MongoDB para novatos', precio: 155},
{ titulo: 'Java el rey', precio: 155},
{ titulo: 'Estupro', precio: 155 }
]
db1>

```
# Ahora para odenar se ocupa .sort (1 o -1). Aquí le decimos que ordene los titulos de manera ascendente (1)

```
db1> db.libros.find({}, {titulo:1, precio:1, _id:0}).sort({titulo:1})
[
{titulo: 'Aprenda PHP', precio: 155},
{ titulo: 'Don quijote', precio: 155},
{ titulo: 'Estupro', precio: 155},
{titulo: 'Java el rey', precio: 155},
{titulo: 'Java en 10 minutos', precio: 155}, {titulo: 'Martin Fierro', precio: 155},
{titulo: 'MongoDB para novatos', precio: 155},
{titulo: 'Python para torpes', precio: 155 }
] db1>

```
# Aquí le digo que lo haga de manera descendente (-1)

```
db1> db.libros.find({}, {titulo:1, precio:1, _id:0}).sort({titulo:-1})
[
titulo: 'Python para torpes', precio: 155},
{ { titulo: 'MongoDB para novatos', precio: 155},
{ titulo: 'Martin Fierro', precio: 155},
{titulo: 'Java en 10 minutos', precio: 155},
'Java el rey', precio: 155},
{titulo: ' { titulo: 'Aprenda PHP', precio: 155 }
{titulo: { titulo: 'Estupro', precio: 155},
Don quijote', precio: 155},
]
db1>

```
# Aquí le digo que me traiga los titulos, precios, y editoriales. Y que ordene los titulos y editoriales de manera ascendente.

```
dbl> db.libros.find({}, {titulo:1, precio:l, editorial:1, id:0}).sort({titulo:l, editorial:1})
[
{titulo: 'Aprenda PHP', editorial: 'Siglo XXI, precio: 155}, {titulo: 'Don quijote', editorial: 'Biblio', precio: 155},
{titulo: 'Estupro', precio: 155},
{titulo: 'Java el rey', editorial: Planeta', precio: 155},
{titulo: 'Java en 10 minutos, editorial: 'Siglo XXI', precio: 155}, {titulo: 'Martin Fierro', editorial: 'Siglo XXI', precio: 155),
{titulo: MongoDB para novatos', editorial: 'Biblio', precio: 155}, {titulo: 'Python para torpes', editorial: 'Planeta', precio: 155 }

```
# Skip (Sirve para saltar algunos documentos al hacer una consulta lo contrario de limit)En esta consulta usando Skip le digo que se SALTE los primeros 2 documentos, y me traiga los demas. Por lo que no me esta mostrando los primeros 2 documentos.

```
db1> db.libros.find({}, { "titulo": 1, "precio": 1, "id": 0, "editorial": 1 }).skip(2) [
{titulo: 'Java en 10 minutos', editorial: 'Siglo XXI, precio: 155}, {titulo: 'Python para torpes',
editorial: 'Planeta', precio: 155}, {titulo: 'Don quijote', editorial: 'Biblio', precio: 155},
{titulo: 'MongoDB para novatos', editorial: 'Biblio', precio: 155}, {titulo: 'Java el rey', editorial: 'Planeta', precio: 155},
{titulo: 'Estupro', precio: 155 }
]
db1>


```

# Size (Sirve para obtener el numero de documentos que tengo en una BD enbase a la consulta que estoy haciendo) se pone despues de un punto (.) despues de la consulta:

```
db1> db.libros.find({},
{"titulo":1, "precio": 1, "_id": 0, "editorial":1})
[
{ titulo: 'Martin Fierro', editorial: 'Siglo XXI', precio: 155},
{ titulo
: 'Aprenda PHP', editorial: 'Siglo XXI', precio: 155},
{ titulo:
'Java en 10 minutos', editorial: 'Siglo XXI', precio: 155},
{ titulo: '
Python para torpes', editorial: 'Planeta', precio: 155}, 'Don quijote', editorial: 'Biblio', precio: 155},
{ titulo:
para novatos', editorial: 'Biblio', precio: 155 }, Java el rey', editorial: 'Planeta', precio: 155},
{ titulo: 'MongoDB
: '
{ titulo
{ titulo : 'Estupro', precio: 155 }

```
# Aquí ya ocupo el size: Pido que me traiga cuandos documentos tengo en la collection libros.

```
db1> db.libros.find({}, { "titulo": 1, "precio": 1, "_id": 0, "editorial": 1 }).size()
8
db1>

```
# Top (Es lo contrario al skip, traer los primeros documentos que yo quiera) En esta consulta me trae los primeros 2 documentos

```
"titulo":
1,
"precio":
1,
"_id":
0, "
editorial":
1 })
.limit(2)
db1> db.libros.find({}, {
[
{titulo: 'Martin Fierro', editorial: 'Siglo XXI', precio: 155}, {titulo: 'Aprenda PHP', editorial: 'Siglo XXI', precio: 155 }
db1>

```
# Drop (Eliminar una colección de una Base de datos): Aquí elimine la colección ejemplo de la base de datos Tienda

```
tienda> db.ejemplo.drop()
true
tienda>

```
# DropDatabase (Eliminar una base de datos) Aquí elimino la base de datos de tienda, luego hago un show dbs para ver las BD y ya no aparece tienda.

```
tienda> db.dropDatabase()
{ok: 1, dropped: 'tienda' }
tienda> show dbs
admin
40.00 KiB
config
108.00 KiB
db1
144.00 KiB
db2
40.00 KiB
local
80.00 KiB
pos_ventas
72.00 KiB
```
