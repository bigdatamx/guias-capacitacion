---
title: Gestión de cluster
---
#Cluster Elasticsearch

Para iniciar:

Un cluster es la colección de dos o mas [nodos](https://www.elastic.co/guide/en/elasticsearch/reference/current/_basic_concepts.html#_node), 
los cuales trabajan en cojunto en el almacenamiento de datos, funcionamiento de indexación
y busquedas federadas. Un Cluster es identificado por un nombre, el cual debe ser unico (por default es "elasticsearch), este nombre es 
importante porque un nodo solo puede ser parte de un cluster por este nombre de identificación. <sup>1</sup>


**Requisitos de instalación:**

**Hardware**

*Memoria*, esta es muy importante porque son el power para realizar las operaciones de "aggregation" y "sorting".

- Ideal 64 GB de memoria RAM 
- Recomendable 32 o 16 Gb de memoria

**CPUs**

Un cluster generalmente utiliza de 2 a 8 nucleos. 


Software

Sistema operativo recomentable: Centos 
 

     
---
<sup>1</sup> Team Elasticsearch, "Basic Concepts",  https://www.elastic.co/guide/en/elasticsearch/reference/current/_basic_concepts.html
