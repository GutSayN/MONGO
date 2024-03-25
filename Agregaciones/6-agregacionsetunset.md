# Agregaciones SET UNSET 
```
[
{
$group:
*_id: The id of the group.
* fieldN: The first field name.
*/
{
_id: "$editorial",
Numero: {
$count: {},
},
media: {
$avg: "$precio",
},
},
},
{
$set:
* field: The field name
* expression: The expression.
{
*/
"Media Total": {
$trunc: ["$media", 2],
},
},
},
{
$unset: "media",
]
```