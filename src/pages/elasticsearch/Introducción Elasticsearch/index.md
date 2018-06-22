---
title: Introducción Elasticsearch
---
#Introducción Elasticsearch

Elasticsearch es un motor open-source para análisis y búsquedas "full-text". Este nos permite almacenar, buscar y analizar grandes volúmenes de datos de forma rápida y casi en tiempo real.



##Conceptos Básicos


####Near Realtime(NRT) 

Elasticsearch esta cerca de bésquedas en tiempo real. No es tiempo real debido a; existe una pequeña latencia (normalmente de un segundo), desde el momento en que se ingresa un nuevo documento, al momento en que se puede buscar.

####Cluster

Un cluster es la unión (colección) de uno más nodos, los cuales permiten almacenar, guardar y brindan la capacidad de realizar consultas a través de todos los nodos.

####Node

Es un único servidor, el cual es parte de un cluster y permite la gestión de los datos.

####Index(índice) 

Un índice es una colección de documentos que tienen características similares.

####Type (Depecrated in 6.0.0)

El tipo toma el valor de una categoría o partición lógica de un índice, este permite guardar información de diferentes tipos en un solo índice.  

###Document

Un documento es unidad básica de información que puede ser ingestada en un indice. This document is expresed in JSON (JavaScript Object Notation)
 
 
###Shards y Replicas

Un índice puede almacenar una gran cantidad de información, la cual puede exceder el limite de hardware de un solo nodo. Esto puede provocar lentitud al realizar peticiones de búsqueda, petciones para agregar nuevos indices, modificación de documentos, etc.

Para resolver el problema de almacenamiento y sus derivados, elasticsearch tiene la habilidad de dividir el indice en multiples piezas llamdas **_shards_**, en temas posteriores se abordara mas adetalle las características de los shards.

Como es bien conocido; existen diversos problemas de red (fallos en lasconexiónes entre servidores, falla en la comunciación con la nube, etc), que pueden presentarse cuando se trabaja con sistemas intercomunicados. Para evitar problemas de red o fallas 
de servidores; es recomendable contar con mecanismos en caso de que se presente algún problema. Para este fin elastcisearch permite permite hacer una o mas copias de shards, las cuales son reconocidas como **_replicas_**.    
  
Para mayor información consultar la [documentación de elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/index.html)
 

 