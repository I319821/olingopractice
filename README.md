# Test Request
## Project:OlingoReadService
Test request:
1. request: service document
http://localhost:8080/OlingoReadService_war/DemoService.svc/?$format=json

result as below:
```
{
"@odata.context": "$metadata",
"value": [
{
"name": "Products",
"url": "Products"
}
]
}
```
request: metadata
http://localhost:8080/OlingoReadService_war/DemoService.svc/$metadata?$format=json

2. result as below:

```
{
"$Version": "4.01",
"OData.Demo": {
"Product": {
"$Kind": "EntityType",
"$Key": [
"ID"
],
"ID": {
"$Type": "Edm.Int32"
},
"Name": {
"$Type": "Edm.String"
},
"Description": {
"$Type": "Edm.String"
}
},
"Container": {
"$Kind": "EntityContainer",
"Products": {
"$Kind": "EntitySet",
"$Type": "OData.Demo.Product"
}
}
}
}
```
3.request: Products entity
http://localhost:8080/OlingoReadService_war/DemoService.svc/Products?$format=json

result as below:

```
{
"@odata.context": "$metadata#Products",
"value": [
{
"ID": 1,
"Name": "Notebook Basic 15",
"Description": "Notebook Basic, 1.7GHz - 15 XGA - 1024MB DDR2 SDRAM - 40GB"
},
{
"ID": 2,
"Name": "1UMTS PDA",
"Description": "Ultrafast 3G UMTS/HSDPA Pocket PC, supports GSM network"
},
{
"ID": 3,
"Name": "Ergo Screen",
"Description": "19 Optimum Resolution 1024 x 768 @ 85Hz, resolution 1280 x 960"
}
]
}
```



---
