# 04-repeat
Cuatro ejemplos usando el repeat

```javascript
.servicios {
    border: 3px solid black;
    height: 300px;
    display: grid;

    /* crea 3 columnas. se puede acortar con repeat */
    /* grid-template-columns: 33.3% 33.3% 33.3%; */

    /* repeat(numero de repeticiones, tamaño) */
    grid-template-columns: repeat(3, 33.3%);

    /* en row crear con repeat dos files */
    grid-template-rows: repeat(2, 50%); /* 3 x 2 = 6 cajas */
}

.servicio {
    color: white;
    text-align: center;
}

.servicio-1 {
    background-color: darkviolet;
}

.servicio-2 {
    background-color: limegreen;
}
.servicio-3 {
    background-color: teal;
}


/* Otro ejemplo de Repeat */
.servicios1 {
    border: 3px solid black;
    height: 300px;
    display: grid;
    /* 1 columna de 50 y dos de 25 */
    grid-template-columns: 50% repeat(2, 25%);
    
    grid-template-rows: repeat(2, 50%);
}

/* Otro ejemplo de Repeat usando shorthand grid*/
.servicios2 {
    border: 3px solid black;
    height: 300px;
    display: grid;
    /* 1 columna de 50 y dos de 25 */
    /* 2 filas */
    /* primero los row y despues column*/
   grid: repeat(2, 50%) / 50% repeat(2, 25%);/*dos row de 50%. 1column de 50% y dos column de 25%*/
}

/* Otro ejemplo de Repeat con distintos paramentros. usando shorthand grid*/
.servicios3 {
    border: 3px solid black;
    height: 300px;
    display: grid;
    /* columnas: Dos de 10% y dos de 40% */
    /* 4 filas */
    /* primero los row y despues column*/
    /* si colocas grid: repeat(1, 50%) solo te tomará los valores de la primera row. 
    height:300 no tomará los valores de las otras filas*/
    /* notar q en el html tendo 16 div. 4 x 4 =16 cajas. es decir, para que tome todo se debe colocar repeat(4, 50%)*/
   grid: repeat(4, 50%) / repeat(2, 10% 40%);
 
}
```
