
# Show dbs / show database:

## Descripción: Permite visualizar las bases de datos existentes.
Uso: show dbs o show database.
Use database:

## Descripción: Se utiliza para seleccionar una base de datos específica o cambiar a una base de datos diferente.
Uso: use nombre_de_la_base_de_datos.
db.createCollection("nombreDeLaColeccion"):

## Descripción: Crea una nueva colección en la base de datos actual.
Uso: db.createCollection("nombre_de_la_coleccion").
Show collections:

## Descripción: Permite listar las colecciones existentes en la base de datos actual.
Uso: show collections.
Cls:

## Descripción: Limpia la pantalla, similar al comando clear.
Uso: cls.
db.nombreDeLaColeccion.insertOne({ }):

## Descripción: Inserta un documento en una colección específica.

Uso: db.nombre_de_la_coleccion.insertOne({ documento }).

OJO ESTO ES IMPORTANTE : Para insertar varios documentos a la vez, se utiliza insertMany en lugar de insertOne.
