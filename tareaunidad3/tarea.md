# AGREGACIONES 2 
# NORMA SUYURI GUTIERREZ CRUZ 
```
test> use ProductosSayu

```

# Inseratar datos : 
```
ProductosSayu> db.producto.insertMany([
... {
...         "codigo": 0,
...         "nombre": "Fantastic Wooden Fish",
...         "unidades": 95,
...         "precio": 291,
...         "fabricante": "Kimberly-Clark",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 1,
...         "nombre": "Rustic Concrete Pants",
...         "unidades": 66,
...         "precio": 279,
...         "fabricante": "Mercury General",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 2,
...         "nombre": "Small Soft Fish",
...         "unidades": 96,
...         "precio": 189,
...         "fabricante": "Primoris Services",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 3,
...         "nombre": "Practical Soft Pants",
...         "unidades": 41,
...         "precio": 67,
...         "fabricante": "Hyatt Hotels",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 4,
...         "nombre": "Ergonomic Metal Ball",
...         "unidades": 5,
...         "precio": 246,
...         "fabricante": "Seaboard",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 5,
...         "nombre": "Small Steel Gloves",
...         "unidades": 45,
...         "precio": 37,
...         "fabricante": "TrueBlue",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 6,
...         "nombre": "Ergonomic Wooden Shirt",
...         "unidades": 63,
...         "precio": 238,
...         "fabricante": "Securian Financial Group",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 7,
...         "nombre": "Handmade Steel Chair",
...         "unidades": 16,
...         "precio": 337,
...         "fabricante": "CIT Group",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 8,
...         "nombre": "Handcrafted Soft Gloves",
...         "unidades": 16,
...         "precio": 282,
...         "fabricante": "Pep Boys-Mann",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 9,
...         "nombre": "Fantastic Concrete Salad",
...         "unidades": 49,
...         "precio": 265,
...         "fabricante": "Kar Auction Services",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 10,
...         "nombre": "Handmade Plastic Hat",
...         "unidades": 7,
...         "precio": 253,
...         "fabricante": "Dick's Sporting Goods",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 11,
...         "nombre": "Refined Wooden Tuna",
...         "unidades": 40,
...         "precio": 212,
...         "fabricante": "WGL Holdings",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 12,
...         "nombre": "Refined Concrete Salad",
...         "unidades": 90,
...         "precio": 129,
...         "fabricante": "Universal Health Services",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 13,
...         "nombre": "Unbranded Soft Fish",
...         "unidades": 53,
...         "precio": 178,
...         "fabricante": "Total System Services",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 14,
...         "nombre": "Small Concrete Fish",
...         "unidades": 40,
...         "precio": 126,
...         "fabricante": "Precision Castparts",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 15,
...         "nombre": "Refined Concrete Bike",
...         "unidades": 15,
...         "precio": 180,
...         "fabricante": "Trinity Industries",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 16,
...         "nombre": "Tasty Cotton Pants",
...         "unidades": 68,
...         "precio": 52,
...         "fabricante": "Cabot",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 17,
...         "nombre": "Incredible Granite Gloves",
...         "unidades": 71,
...         "precio": 290,
...         "fabricante": "Oneok",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 18,
...         "nombre": "Practical Metal Mouse",
...         "unidades": 35,
...         "precio": 190,
...         "fabricante": "National Oilwell Varco",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 19,
...         "nombre": "Handcrafted Steel Chicken",
...         "unidades": 55,
...         "precio": 113,
...         "fabricante": "State Street Corp.",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 20,
...         "nombre": "Ergonomic Metal Table",
...         "unidades": 0,
...         "precio": 94,
...         "fabricante": "Kelly Services",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 21,
...         "nombre": "Tasty Wooden Ball",
...         "unidades": 18,
...         "precio": 76,
...         "fabricante": "State Farm Insurance Cos.",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 22,
...         "nombre": "Unbranded Soft Table",
...         "unidades": 41,
...         "precio": 284,
...         "fabricante": "Motorola Solutions",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 23,
...         "nombre": "Handcrafted Metal Tuna",
...         "unidades": 63,
...         "precio": 320,
...         "fabricante": "Williams-Sonoma",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 24,
...         "nombre": "Incredible Frozen Shirt",
...         "unidades": 37,
...         "precio": 173,
...         "fabricante": "Hawaiian Holdings",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 25,
...         "nombre": "Licensed Fresh Chicken",
...         "unidades": 65,
...         "precio": 233,
...         "fabricante": "Kemper",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 26,
...         "nombre": "Intelligent Plastic Bike",
...         "unidades": 39,
...         "precio": 241,
...         "fabricante": "Tractor Supply",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 27,
...         "nombre": "Sleek Steel Chicken",
...         "unidades": 47,
...         "precio": 131,
...         "fabricante": "Mondelez International",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 28,
...         "nombre": "Handcrafted Granite Cheese",
...         "unidades": 27,
...         "precio": 304,
...         "fabricante": "Lennar",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 29,
...         "nombre": "Unbranded Soft Computer",
...         "unidades": 33,
...         "precio": 69,
...         "fabricante": "Delta Tucker Holdings",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 30,
...         "nombre": "Small Rubber Pants",
...         "unidades": 89,
...         "precio": 16,
...         "fabricante": "Hanesbrands",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 31,
...         "nombre": "Generic Fresh Keyboard",
...         "unidades": 69,
...         "precio": 16,
...         "fabricante": "WestRock",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 32,
...         "nombre": "Sleek Soft Towels",
...         "unidades": 68,
...         "precio": 68,
...         "fabricante": "Alere",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 33,
...         "nombre": "Generic Concrete Hat",
...         "unidades": 82,
...         "precio": 70,
...         "fabricante": "American Tire Distributors Holdings",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 34,
...         "nombre": "Practical Cotton Keyboard",
...         "unidades": 43,
...         "precio": 25,
...         "fabricante": "AutoNation",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 35,
...         "nombre": "Sleek Frozen Hat",
...         "unidades": 40,
...         "precio": 110,
...         "fabricante": "Pool",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 36,
...         "nombre": "Rustic Soft Table",
...         "unidades": 73,
...         "precio": 331,
...         "fabricante": "Werner Enterprises",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 37,
...         "nombre": "Awesome Soft Gloves",
...         "unidades": 35,
...         "precio": 18,
...         "fabricante": "Anthem",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 38,
...         "nombre": "Rustic Steel Shoes",
...         "unidades": 39,
...         "precio": 257,
...         "fabricante": "Universal American",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 39,
...         "nombre": "Handmade Soft Chips",
...         "unidades": 56,
...         "precio": 208,
...         "fabricante": "State Farm Insurance Cos.",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 40,
...         "nombre": "Handmade Frozen Salad",
...         "unidades": 13,
...         "precio": 85,
...         "fabricante": "Nordstrom",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 41,
...         "nombre": "Awesome Cotton Cheese",
...         "unidades": 56,
...         "precio": 277,
...         "fabricante": "HealthSouth",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 42,
...         "nombre": "Licensed Granite Ball",
...         "unidades": 74,
...         "precio": 92,
...         "fabricante": "SunPower",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 43,
...         "nombre": "Sleek Frozen Table",
...         "unidades": 50,
...         "precio": 77,
...         "fabricante": "Archrock",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 44,
...         "nombre": "Sleek Steel Ball",
...         "unidades": 36,
...         "precio": 236,
...         "fabricante": "TransDigm Group",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 45,
...         "nombre": "Fantastic Soft Pants",
...         "unidades": 78,
...         "precio": 103,
...         "fabricante": "TEGNA",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 46,
...         "nombre": "Intelligent Metal Bike",
...         "unidades": 16,
...         "precio": 141,
...         "fabricante": "Core-Mark Holding",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 47,
...         "nombre": "Practical Frozen Chips",
...         "unidades": 0,
...         "precio": 305,
...         "fabricante": "Delta Air Lines",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 48,
...         "nombre": "Refined Plastic Hat",
...         "unidades": 52,
...         "precio": 81,
...         "fabricante": "Wendy's",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 49,
...         "nombre": "Licensed Concrete Soap",
...         "unidades": 21,
...         "precio": 68,
...         "fabricante": "First Solar",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 50,
...         "nombre": "Awesome Frozen Shoes",
...         "unidades": 33,
...         "precio": 125,
...         "fabricante": "Comerica",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 51,
...         "nombre": "Fantastic Metal Pants",
...         "unidades": 5,
...         "precio": 129,
...         "fabricante": "OneMain Holdings",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 52,
...         "nombre": "Ergonomic Metal Hat",
...         "unidades": 25,
...         "precio": 85,
...         "fabricante": "Kar Auction Services",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 53,
...         "nombre": "Licensed Plastic Hat",
...         "unidades": 96,
...         "precio": 38,
...         "fabricante": "Best Buy",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 54,
...         "nombre": "Generic Metal Sausages",
...         "unidades": 84,
...         "precio": 77,
...         "fabricante": "DST Systems",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 55,
...         "nombre": "Small Metal Tuna",
...         "unidades": 46,
...         "precio": 43,
...         "fabricante": "Raymond James Financial",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 56,
...         "nombre": "Intelligent Frozen Sausages",
...         "unidades": 3,
...         "precio": 111,
...         "fabricante": "A.O. Smith",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 57,
...         "nombre": "Practical Fresh Fish",
...         "unidades": 69,
...         "precio": 331,
...         "fabricante": "Hartford Financial Services Group",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 58,
...         "nombre": "Refined Concrete Shirt",
...         "unidades": 57,
...         "precio": 49,
...         "fabricante": "Simon Property Group",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 59,
...         "nombre": "Handcrafted Granite Chicken",
...         "unidades": 26,
...         "precio": 164,
...         "fabricante": "Comcast",
...         "tipo": "medio"
...     },
...     {
...         "codigo": 60,
...         "nombre": "Practical Frozen Salad",
...         "unidades": 43,
...         "precio": 250,
...         "fabricante": "Nasdaq OMX Group",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 61,
...         "nombre": "Sleek Rubber Keyboard",
...         "unidades": 82,
...         "precio": 33,
...         "fabricante": "Alere",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 62,
...         "nombre": "Ergonomic Steel Fish",
...         "unidades": 10,
...         "precio": 94,
...         "fabricante": "HCA Holdings",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 63,
...         "nombre": "Rustic Plastic Mouse",
...         "unidades": 5,
...         "precio": 24,
...         "fabricante": "Orbital ATK",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 64,
...         "nombre": "Awesome Cotton Mouse",
...         "unidades": 39,
...         "precio": 285,
...         "fabricante": "Telephone & Data Systems",
...         "tipo": "basico"
...     },
...     {
...         "codigo": 65,
...         "nombre": "Intelligent Soft Towels",
...         "unidades": 19,
...         "precio": 93,
...         "fabricante": "Ascena Retail Group",
...         "tipo": "avanzado"
...     },
...     {
...         "codigo": 66,
...         "nombre": "Incredible Concrete Fish",
...         "unidades": 96,
...         "precio": 336,
...         "fabricante": "Darling Ingredients",
...         "tipo": "medio"
...     }]);
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6615ed3f16ec171de4d14a0e'),
    '1': ObjectId('6615ed3f16ec171de4d14a0f'),
    '2': ObjectId('6615ed3f16ec171de4d14a10'),
    '3': ObjectId('6615ed3f16ec171de4d14a11'),
    '4': ObjectId('6615ed3f16ec171de4d14a12'),
    '5': ObjectId('6615ed3f16ec171de4d14a13'),
    '6': ObjectId('6615ed3f16ec171de4d14a14'),
    '7': ObjectId('6615ed3f16ec171de4d14a15'),
    '8': ObjectId('6615ed3f16ec171de4d14a16'),
    '9': ObjectId('6615ed3f16ec171de4d14a17'),
    '10': ObjectId('6615ed3f16ec171de4d14a18'),
    '11': ObjectId('6615ed3f16ec171de4d14a19'),
    '12': ObjectId('6615ed3f16ec171de4d14a1a'),
    '13': ObjectId('6615ed3f16ec171de4d14a1b'),
    '14': ObjectId('6615ed3f16ec171de4d14a1c'),
    '15': ObjectId('6615ed3f16ec171de4d14a1d'),
    '16': ObjectId('6615ed3f16ec171de4d14a1e'),
    '17': ObjectId('6615ed3f16ec171de4d14a1f'),
    '18': ObjectId('6615ed3f16ec171de4d14a20'),
    '19': ObjectId('6615ed3f16ec171de4d14a21'),
    '20': ObjectId('6615ed3f16ec171de4d14a22'),
    '21': ObjectId('6615ed3f16ec171de4d14a23'),
    '22': ObjectId('6615ed3f16ec171de4d14a24'),
    '23': ObjectId('6615ed3f16ec171de4d14a25'),
    '24': ObjectId('6615ed3f16ec171de4d14a26'),
    '25': ObjectId('6615ed3f16ec171de4d14a27'),
    '26': ObjectId('6615ed3f16ec171de4d14a28'),
    '27': ObjectId('6615ed3f16ec171de4d14a29'),
    '28': ObjectId('6615ed3f16ec171de4d14a2a'),
    '29': ObjectId('6615ed3f16ec171de4d14a2b'),
    '30': ObjectId('6615ed3f16ec171de4d14a2c'),
    '31': ObjectId('6615ed3f16ec171de4d14a2d'),
    '32': ObjectId('6615ed3f16ec171de4d14a2e'),
    '33': ObjectId('6615ed3f16ec171de4d14a2f'),
    '34': ObjectId('6615ed3f16ec171de4d14a30'),
    '35': ObjectId('6615ed3f16ec171de4d14a31'),
    '36': ObjectId('6615ed3f16ec171de4d14a32'),
    '37': ObjectId('6615ed3f16ec171de4d14a33'),
    '38': ObjectId('6615ed3f16ec171de4d14a34'),
    '39': ObjectId('6615ed3f16ec171de4d14a35'),
    '40': ObjectId('6615ed3f16ec171de4d14a36'),
    '41': ObjectId('6615ed3f16ec171de4d14a37'),
    '42': ObjectId('6615ed3f16ec171de4d14a38'),
    '43': ObjectId('6615ed3f16ec171de4d14a39'),
    '44': ObjectId('6615ed3f16ec171de4d14a3a'),
    '45': ObjectId('6615ed3f16ec171de4d14a3b'),
    '46': ObjectId('6615ed3f16ec171de4d14a3c'),
    '47': ObjectId('6615ed3f16ec171de4d14a3d'),
    '48': ObjectId('6615ed3f16ec171de4d14a3e'),
    '49': ObjectId('6615ed3f16ec171de4d14a3f'),
    '50': ObjectId('6615ed3f16ec171de4d14a40'),
    '51': ObjectId('6615ed3f16ec171de4d14a41'),
    '52': ObjectId('6615ed3f16ec171de4d14a42'),
    '53': ObjectId('6615ed3f16ec171de4d14a43'),
    '54': ObjectId('6615ed3f16ec171de4d14a44'),
    '55': ObjectId('6615ed3f16ec171de4d14a45'),
    '56': ObjectId('6615ed3f16ec171de4d14a46'),
    '57': ObjectId('6615ed3f16ec171de4d14a47'),
    '58': ObjectId('6615ed3f16ec171de4d14a48'),
    '59': ObjectId('6615ed3f16ec171de4d14a49'),
    '60': ObjectId('6615ed3f16ec171de4d14a4a'),
    '61': ObjectId('6615ed3f16ec171de4d14a4b'),
    '62': ObjectId('6615ed3f16ec171de4d14a4c'),
    '63': ObjectId('6615ed3f16ec171de4d14a4d'),
    '64': ObjectId('6615ed3f16ec171de4d14a4e'),
    '65': ObjectId('6615ed3f16ec171de4d14a4f'),
    '66': ObjectId('6615ed3f16ec171de4d14a50')
  }
}
```
# 1. Contar los productos de tipo "medio" usando un método básico
```
ProductosSayu> db.producto.count({ tipo: "medio" });
DeprecationWarning: Collection.count() is deprecated. Use countDocuments or estimatedDocumentCount.
```

# 2. Indicar con un distinct, las empresas (fabricantes) que hay en la colección
```
ProductosSayu> db.producto.distinct("fabricante");
[
  'A.O. Smith',
  'Alere',
  'American Tire Distributors Holdings',
  'Anthem',
  'Archrock',
  'Ascena Retail Group',
  'AutoNation',
  'Best Buy',
  'CIT Group',
  'Cabot',
  'Comcast',
  'Comerica',
  'Core-Mark Holding',
  'DST Systems',
  'Darling Ingredients',
  'Delta Air Lines',
  'Delta Tucker Holdings',
  "Dick's Sporting Goods",
  'First Solar',
  'HCA Holdings',
  'Hanesbrands',
  'Hartford Financial Services Group',
  'Hawaiian Holdings',
  'HealthSouth',
  'Hyatt Hotels',
  'Kar Auction Services',
  'Kelly Services',
  'Kemper',
  'Kimberly-Clark',
  'Lennar',
  'Mercury General',
  'Mondelez International',
  'Motorola Solutions',
  'Nasdaq OMX Group',
  'National Oilwell Varco',
  'Nordstrom',
  'OneMain Holdings',
  'Oneok',
  'Orbital ATK',
  'Pep Boys-Mann',
  'Pool',
  'Precision Castparts',
  'Primoris Services',
  'Raymond James Financial',
  'Seaboard',
  'Securian Financial Group',
  'Simon Property Group',
  'State Farm Insurance Cos.',
  'State Street Corp.',
  'SunPower',
  'TEGNA',
  'Telephone & Data Systems',
  'Total System Services',
  'Tractor Supply',
  'TransDigm Group',
  'Trinity Industries',
  'TrueBlue',
  'Universal American',
  'Universal Health Services',
  'WGL Holdings',
  "Wendy's",
  'Werner Enterprises',
  'WestRock',
  'Williams-Sonoma'
]
```
# 3. Usando aggregate, visualizar los productos que tengan más de 80 unidades

``` ProductosSayu> db.producto.aggregate([ { $match: { unidades: { $gt: 80 } } }] );
[
  {
    _id: ObjectId('6615ed3f16ec171de4d14a0e'),
    codigo: 0,
    nombre: 'Fantastic Wooden Fish',
    unidades: 95,
    precio: 291,
    fabricante: 'Kimberly-Clark',
    tipo: 'avanzado'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a10'),
    codigo: 2,
    nombre: 'Small Soft Fish',
    unidades: 96,
    precio: 189,
    fabricante: 'Primoris Services',
    tipo: 'medio'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a1a'),
    codigo: 12,
    nombre: 'Refined Concrete Salad',
    unidades: 90,
    precio: 129,
    fabricante: 'Universal Health Services',
    tipo: 'avanzado'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a2c'),
    codigo: 30,
    nombre: 'Small Rubber Pants',
    unidades: 89,
    precio: 16,
    fabricante: 'Hanesbrands',
    tipo: 'basico'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a2f'),
    codigo: 33,
    nombre: 'Generic Concrete Hat',
    unidades: 82,
    precio: 70,
    fabricante: 'American Tire Distributors Holdings',
    tipo: 'basico'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a43'),
    codigo: 53,
    nombre: 'Licensed Plastic Hat',
    unidades: 96,
    precio: 38,
    fabricante: 'Best Buy',
    tipo: 'medio'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a44'),
    codigo: 54,
    nombre: 'Generic Metal Sausages',
    unidades: 84,
    precio: 77,
    fabricante: 'DST Systems',
    tipo: 'medio'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a4b'),
    codigo: 61,
    nombre: 'Sleek Rubber Keyboard',
    unidades: 82,
    precio: 33,
    fabricante: 'Alere',
    tipo: 'basico'
  },
  {
    _id: ObjectId('6615ed3f16ec171de4d14a50'),
    codigo: 66,
    nombre: 'Incredible Concrete Fish',
    unidades: 96,
    precio: 336,
    fabricante: 'Darling Ingredients',
    tipo: 'medio'
  }


```


# 4. Con $project visualizar solo el nombre, unidades y precio de los productos que tengan menos de 10 unidades

``` ProductosSayu> db.producto.aggregate([
...     { $match: { unidades: { $lt: 10 } } },
...     { $project: { _id: 0, nombre: 1, unidades: 1, precio: 1 } }
... ]);
[
  { nombre: 'Ergonomic Metal Ball', unidades: 5, precio: 246 },
  { nombre: 'Handmade Plastic Hat', unidades: 7, precio: 253 },
  { nombre: 'Ergonomic Metal Table', unidades: 0, precio: 94 },
  { nombre: 'Practical Frozen Chips', unidades: 0, precio: 305 },
  { nombre: 'Fantastic Metal Pants', unidades: 5, precio: 129 },
  { nombre: 'Intelligent Frozen Sausages', unidades: 3, precio: 111 },
  { nombre: 'Rustic Plastic Mouse', unidades: 5, precio: 24 }
]
```



# 5. Con $project ponemos el fabricante, pero le cambiamos el nombre por “empresa”.Usamos el mismo comando anterior

``` ProductosSayu> db.producto.aggregate([
...     { $project: { _id: 0, empresa: "$fabricante" } }
... ]);
[
  { empresa: 'Kimberly-Clark' },
  { empresa: 'Mercury General' },
  { empresa: 'Primoris Services' },
  { empresa: 'Hyatt Hotels' },
  { empresa: 'Seaboard' },
  { empresa: 'TrueBlue' },
  { empresa: 'Securian Financial Group' },
  { empresa: 'CIT Group' },
  { empresa: 'Pep Boys-Mann' },
  { empresa: 'Kar Auction Services' },
  { empresa: "Dick's Sporting Goods" },
  { empresa: 'WGL Holdings' },
  { empresa: 'Universal Health Services' },
  { empresa: 'Total System Services' },
  { empresa: 'Precision Castparts' },
  { empresa: 'Trinity Industries' },
  { empresa: 'Cabot' },
  { empresa: 'Oneok' },
  { empresa: 'National Oilwell Varco' },
  { empresa: 'State Street Corp.' }
]
Type "it" for more
```
# 6. Añadir a la consulta anterior un campo calculado que se llame total y que multiplique precio por unidades.

``` ProductosSayu> db.producto.aggregate([
...     { $project: { _id: 0, empresa: "$fabricante", total: { $multiply: ["$precio", "$unidades"] } } }
... ]);
[
  { empresa: 'Kimberly-Clark', total: 27645 },
  { empresa: 'Mercury General', total: 18414 },
  { empresa: 'Primoris Services', total: 18144 },
  { empresa: 'Hyatt Hotels', total: 2747 },
  { empresa: 'Seaboard', total: 1230 },
  { empresa: 'TrueBlue', total: 1665 },
  { empresa: 'Securian Financial Group', total: 14994 },
  { empresa: 'CIT Group', total: 5392 },
  { empresa: 'Pep Boys-Mann', total: 4512 },
  { empresa: 'Kar Auction Services', total: 12985 },
  { empresa: "Dick's Sporting Goods", total: 1771 },
  { empresa: 'WGL Holdings', total: 8480 },
  { empresa: 'Universal Health Services', total: 11610 },
  { empresa: 'Total System Services', total: 9434 },
  { empresa: 'Precision Castparts', total: 5040 },
  { empresa: 'Trinity Industries', total: 2700 },
  { empresa: 'Cabot', total: 3536 },
  { empresa: 'Oneok', total: 20590 },
  { empresa: 'National Oilwell Varco', total: 6650 },
  { empresa: 'State Street Corp.', total: 6215 }
]


```
# 7. Hacer que el nombre salga en mayúsculas con el operador $toUpper
``` ProductosSayu> db.producto.aggregate([
...     { $project: { _id: 0, nombre_en_mayusculas: { $toUpper: "$nombre" } } }
... ]);
[
  { nombre_en_mayusculas: 'FANTASTIC WOODEN FISH' },
  { nombre_en_mayusculas: 'RUSTIC CONCRETE PANTS' },
  { nombre_en_mayusculas: 'SMALL SOFT FISH' },
  { nombre_en_mayusculas: 'PRACTICAL SOFT PANTS' },
  { nombre_en_mayusculas: 'ERGONOMIC METAL BALL' },
  { nombre_en_mayusculas: 'SMALL STEEL GLOVES' },
  { nombre_en_mayusculas: 'ERGONOMIC WOODEN SHIRT' },
  { nombre_en_mayusculas: 'HANDMADE STEEL CHAIR' },
  { nombre_en_mayusculas: 'HANDCRAFTED SOFT GLOVES' },
  { nombre_en_mayusculas: 'FANTASTIC CONCRETE SALAD' },
  { nombre_en_mayusculas: 'HANDMADE PLASTIC HAT' },
  { nombre_en_mayusculas: 'REFINED WOODEN TUNA' },
  { nombre_en_mayusculas: 'REFINED CONCRETE SALAD' },
  { nombre_en_mayusculas: 'UNBRANDED SOFT FISH' },
  { nombre_en_mayusculas: 'SMALL CONCRETE FISH' },
  { nombre_en_mayusculas: 'REFINED CONCRETE BIKE' },
  { nombre_en_mayusculas: 'TASTY COTTON PANTS' },
  { nombre_en_mayusculas: 'INCREDIBLE GRANITE GLOVES' },
  { nombre_en_mayusculas: 'PRACTICAL METAL MOUSE' },
  { nombre_en_mayusculas: 'HANDCRAFTED STEEL CHICKEN' }
]

```
# 8. Añadir un campo calculado que ponga el nombre del producto y el tipo concatenado con el operador $concat. Le llamamos al campo “completo”
```
ProductosSayu> db.producto.aggregate([
...     { $project: { _id: 0, completo: { $concat: ["$nombre", " - ", "$tipo"] } } }
... ]);
[
  { completo: 'Fantastic Wooden Fish - avanzado' },
  { completo: 'Rustic Concrete Pants - medio' },
  { completo: 'Small Soft Fish - medio' },
  { completo: 'Practical Soft Pants - avanzado' },
  { completo: 'Ergonomic Metal Ball - medio' },
  { completo: 'Small Steel Gloves - avanzado' },
  { completo: 'Ergonomic Wooden Shirt - avanzado' },
  { completo: 'Handmade Steel Chair - medio' },
  { completo: 'Handcrafted Soft Gloves - basico' },
  { completo: 'Fantastic Concrete Salad - basico' },
  { completo: 'Handmade Plastic Hat - medio' },
  { completo: 'Refined Wooden Tuna - avanzado' },
  { completo: 'Refined Concrete Salad - avanzado' },
  { completo: 'Unbranded Soft Fish - basico' },
  { completo: 'Small Concrete Fish - medio' },
  { completo: 'Refined Concrete Bike - basico' },
  { completo: 'Tasty Cotton Pants - basico' },
  { completo: 'Incredible Granite Gloves - avanzado' },
  { completo: 'Practical Metal Mouse - basico' },
  { completo: 'Handcrafted Steel Chicken - medio' }
]

```


# 9. Ordena el resultado por el campo “total”

``` ProductosSayu> db.producto.aggregate([
...     { $project: { _id: 0, nombre: 1, unidades: 1, precio: 1, total: { $multiply: ["$precio", "$unidades"] } } },
...     { $sort: { total: 1 } }
... ]);
[
  {
    nombre: 'Ergonomic Metal Table',
    unidades: 0,
    precio: 94,
    total: 0
  },
  {
    nombre: 'Practical Frozen Chips',
    unidades: 0,
    precio: 305,
    total: 0
  },
  {
    nombre: 'Rustic Plastic Mouse',
    unidades: 5,
    precio: 24,
    total: 120
  },
  {
    nombre: 'Intelligent Frozen Sausages',
    unidades: 3,
    precio: 111,
    total: 333
  },
  {
    nombre: 'Awesome Soft Gloves',
    unidades: 35,
    precio: 18,
    total: 630
  },
  {
    nombre: 'Fantastic Metal Pants',
    unidades: 5,
    precio: 129,
    total: 645
  },
  {
    nombre: 'Ergonomic Steel Fish',
    unidades: 10,
    precio: 94,
    total: 940
  },
  {
    nombre: 'Practical Cotton Keyboard',
    unidades: 43,
    precio: 25,
    total: 1075
  },
  {
    nombre: 'Generic Fresh Keyboard',
    unidades: 69,
    precio: 16,
    total: 1104
  },
  {
    nombre: 'Handmade Frozen Salad',
    unidades: 13,
    precio: 85,
    total: 1105
  },
  {
    nombre: 'Ergonomic Metal Ball',
    unidades: 5,
    precio: 246,
    total: 1230
  },
  {
    nombre: 'Tasty Wooden Ball',
    unidades: 18,
    precio: 76,
    total: 1368
  },
  {
    nombre: 'Small Rubber Pants',
    unidades: 89,
    precio: 16,
    total: 1424
  },
  {
    nombre: 'Licensed Concrete Soap',
    unidades: 21,
    precio: 68,
    total: 1428
  },
  {
    nombre: 'Small Steel Gloves',
    unidades: 45,
    precio: 37,
    total: 1665
  },
  {
    nombre: 'Intelligent Soft Towels',
    unidades: 19,
    precio: 93,
    total: 1767
  },
  {
    nombre: 'Handmade Plastic Hat',
    unidades: 7,
    precio: 253,
    total: 1771
  },
  { nombre: 'Small Metal Tuna', unidades: 46, precio: 43, total: 1978 },
  {
    nombre: 'Ergonomic Metal Hat',
    unidades: 25,
    precio: 85,
    total: 2125
  },
  {
    nombre: 'Intelligent Metal Bike',
    unidades: 16,
    precio: 141,
    total: 2256
  }
]

```

# 10. Haciendo una nueva consulta, averiguar el numero de productos por tipo de producto
```
ProductosSayu> db.producto.aggregate([
...     { $group: { _id: "$tipo", total_productos: { $sum: 1 } } }
... ]);
[
  { _id: 'basico', total_productos: 24 },
  { _id: 'avanzado', total_productos: 18 },
  { _id: 'medio', total_productos: 25 }
]

```
# 11. Añadir el valor mayor y el menor

``` ProductosSayu> db.producto.aggregate([
...     { $group: { _id: null, max_precio: { $max: "$precio" }, min_precio: { $min: "$precio" } } }
... ]);
[ { _id: null, max_precio: 337, min_precio: 16 } ]
```

# 12. Añade el total de unidades por cada tipo
``` 
 db.producto.aggregate([
...     { $group: { _id: "$tipo", total_unidades: { $sum: "$unidades" } } }
... ]);
[
  { _id: 'avanzado', total_unidades: 773 },
  { _id: 'medio', total_unidades: 1224 },
  { _id: 'basico', total_unidades: 1067 }
]
```
# 13. Con el operador $set y el operador “$substr” visualiza todos los datos del producto"Small Metal Tuna" y los primeros 5 caracteres del nombre
```
ProductosSayu> db.producto.aggregate([
...     { $match: { nombre: "Small Metal Tuna" } },
...     { $project: { nombre: { $substr: ["$nombre", 0, 5] }, unidades: 1, precio: 1, fabricante: 1, tipo: 1 } }
... ]);
[
  {
    _id: ObjectId('6615ed3f16ec171de4d14a45'),
    unidades: 46,
    precio: 43,
    fabricante: 'Raymond James Financial',
    tipo: 'medio',
    nombre: 'Small'
  }
]

```
# 14. Creamos una salida que tenga el nombre del articulo y el total (precio por unidades) y lo guardamos en una colección denominada productos2

``` db.producto.aggregate([
...     { $project: { _id: 0, nombre: 1, total: { $multiply: ["$precio", "$unidades"] } } },
...     { $out: "productos2" }
... ]);
``` 


# 15. Creamos una salida que tenga el nombre del articulo y el total (precio por unidades) y lo guardamos en una colección denominada productos2
``` ProductosSayu> db.getCollectionNames();
[ 'producto', 'productos2' ]
```


 # 16. Comprobamos que se ha creado
``` 
ProductosSayu> db.getCollectionNames();
[ 'producto', 'productos2' ]
```

17. Hacemos un find para comprobar el resultado

```
ProductosSayu> db.productos2.find();
[
  {
    _id: ObjectId('6615f43fcfc5bcf06421632c'),
    nombre: 'Fantastic Wooden Fish',
    total: 27645
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421632d'),
    nombre: 'Rustic Concrete Pants',
    total: 18414
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421632e'),
    nombre: 'Small Soft Fish',
    total: 18144
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421632f'),
    nombre: 'Practical Soft Pants',
    total: 2747
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216330'),
    nombre: 'Ergonomic Metal Ball',
    total: 1230
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216331'),
    nombre: 'Small Steel Gloves',
    total: 1665
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216332'),
    nombre: 'Ergonomic Wooden Shirt',
    total: 14994
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216333'),
    nombre: 'Handmade Steel Chair',
    total: 5392
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216334'),
    nombre: 'Handcrafted Soft Gloves',
    total: 4512
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216335'),
    nombre: 'Fantastic Concrete Salad',
    total: 12985
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216336'),
    nombre: 'Handmade Plastic Hat',
    total: 1771
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216337'),
    nombre: 'Refined Wooden Tuna',
    total: 8480
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216338'),
    nombre: 'Refined Concrete Salad',
    total: 11610
  },
  {
    _id: ObjectId('6615f43fcfc5bcf064216339'),
    nombre: 'Unbranded Soft Fish',
    total: 9434
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421633a'),
    nombre: 'Small Concrete Fish',
    total: 5040
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421633b'),
    nombre: 'Refined Concrete Bike',
    total: 2700
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421633c'),
    nombre: 'Tasty Cotton Pants',
    total: 3536
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421633d'),
    nombre: 'Incredible Granite Gloves',
    total: 20590
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421633e'),
    nombre: 'Practical Metal Mouse',
    total: 6650
  },
  {
    _id: ObjectId('6615f43fcfc5bcf06421633f'),
    nombre: 'Handcrafted Steel Chicken',
    total: 6215
  }
]
``` 