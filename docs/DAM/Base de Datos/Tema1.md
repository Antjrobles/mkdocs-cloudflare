---
type: b7179839-30ff-4f73-b5ed-073b6e9789e2
title: BD - UNIDAD 1
icon: null
createdAt: '2023-11-14T10:58:40.713Z'
creationDate: 2023-11-14 11:58
modificationDate: 2024-01-13 10:10
tags: []
coverImage: base-de-datos-min-e1523470739502
author: null
---



> # BASE DE DATOS

- Tutora => Laura Plaza Ruiz



> ## MÉTODOS DE ACCESO



- Secuencial => Encadenado

- Secuencial indexado 

- Directo => Accesso directo, Acceso indexado, Acceso calculado (Hash)





---



> ## TIPOS DE FICHEROS



- FICHEROS SECUENCIALES

- FICHEROS DE ACCESO DIRECTO




---


> ## ORACLE DATABASE

- version 18c => [https://www.oracle.com/database/technologies/xe18c-downloads.html](https://www.oracle.com/database/technologies/xe18c-downloads.html)

- version 21c => [https://www.oracle.com/es/database/technologies/appdev/xe/quickstart.html](https://www.oracle.com/es/database/technologies/appdev/xe/quickstart.html)



- Pequeña guia de introduccion => [https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392683/mod_resource/content/2/BD01_Contenidos_Imprimible/BD01_AccesoSys_creausuario.pdf](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392683/mod_resource/content/2/BD01_Contenidos_Imprimible/BD01_AccesoSys_creausuario.pdf)



```sql
/* BASIC COMMANDS */

/* Connect to sqlplus */
sqlplus sys as sysdba

/*PASSWORD resina */

/* Show user */
show user con_name

/* Create user */
create user c##antjrobles identified by anjrobles default tablespace users;

/* Grant access */  /* IMPORTANT, when asked for password must be different from the root password. This is the the password for that specific user. Usually same as user, for exmaple antjrobles */
grant connect, resource, DBA to c##antjrobles;

/* Connect to user */
CONNECT c##antjrobles
show user con_ name /* to check connection success */
```



---



