---
title: Mapeo y analizadores de texto.
---
#Mapeo y analizadores de texto

Este apartado tiene como objetivo dar a conocer el uso del mapping, asi como, los analizadores de texto y su función. Antes adentrarse al tema de analizadores; es importante conocer el termino y el sudo del mapeo: 

El **mapeo (mapping)** es uno de los conceptos más utlizados e importantes de elastisearch. Los mapping son los encargados de definir la estructura; para realizar el procesamiento de de los documentos.

Es importante conocer dos conceptos que serán utilizados en este apartado:

- *Indexación (Indexing):* Define la acción de almacenar, indexar y procesar un documento dentro de un indice. 
- *Búsqueda (Searching):*  Define la acción para obtener la información o los datos desde un indice.

Cuando se habla de mapeo, elasticsearch tiene la habilidad de crear mappings, si no se encuentran definidos al realizar una indexación. Los indices creados tienen la estructura definida en base a los datos de la indexación.

##Cración de mapping por *Indexación* (explicit mapping creation)

Cuando  se esta trabajando con un indice nuevo; elasticsearch nos permite
 crearlo, al realizar la indexación de un documento nuevo, lo anterior generará
 de forma automátca un nuevo indice que satisfaga las necesidades del documento, 
 basado en la información contenida en la petición.
 
 Ejemplo
 
 Se desea crear un indice que contenga los datos de los jugadores y sus anotaciones:
 
 Atributos: nombre, apellido, goles, asistencias.
 
 ```
 curl -XPOST "http://localhost:9200/futbol/jugadores" -H 'Content-Type: application/json' -d'
 {
   "nombre":"Alejandro",
   "apellido":"Almaraz",
   "goles":[12,1,22],
   "asistencias":[4,12,55]
 }'
 
 ```
  
 Al ejecutar el comando anterior nos generará el siguiente mapping (paara consultar el mapeo de un indice utilizar el metodo GET y el nombre del indice)
 
 ```
  curl -XGET "http://127.0.0.1:9200/futbol?pretty"
 ```
 
 Resultado
 
 ```JSON
 {
   "futbol" : {
     "aliases" : { },
     "mappings" : {
       "jugadores" : {
         "properties" : {
           "apellido" : {
             "type" : "text",
             "fields" : {
               "keyword" : {
                 "type" : "keyword",
                 "ignore_above" : 256
               }
             }
           },
           "asistencias" : {
             "type" : "long"
           },
           "goles" : {
             "type" : "long"
           },
           "nombre" : {
             "type" : "text",
             "fields" : {
               "keyword" : {
                 "type" : "keyword",
                 "ignore_above" : 256
               }
             }
           }
         }
       }
     },
     "settings" : {
       "index" : {
         "creation_date" : "1529964141573",
         "number_of_shards" : "5",
         "number_of_replicas" : "1",
         "uuid" : "n-9_IFlMQ2GrQUTsS4gSHw",
         "version" : {
           "created" : "5060899"
         },
         "provided_name" : "futbol"
       }
     }
   }
 }

 ```
       

