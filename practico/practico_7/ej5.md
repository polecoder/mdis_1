# Ejercicio 5

## Consigna

Demostrar que en un conjunto con 61 personas hay al menos 13 personas cada una de las cuales desciende de la siguiente o hay un al menos 6 personas tales que ninguna de ellas desciende de otra.

## Resolución

Demostremos este problema por absurdo. Llamemos a las condiciones dadas de la siguiente forma:

- $A$: Hay al menos 13 personas cada una de las cuales desciende de la siguiente.

- $B$: Hay al menos 6 personas tales que ninguna de ellas desciende de otra.

Queremos probar que si no se cumple $A$, entonces necesariamente se tiene que cumplir $B$.

Supongamos que no se cumple $A$. Entonces la cadena de mayor tamaño posible es de 12 personas. Acomodemos el resto de las personas de forma de incluir la mayor cantidad de personas posibles en el esquema (sin incrementar el tamaño máximo de cadena). Esto se logra agregando más cadenas de 12 personas hasta que no se puedan agregar más. Al llegar a 5 cadenas de 12, observemos que tenemos 60 personas. Si agregamos una persona más como descendiente de otra, entonces se cumpliría $A$. Por lo tanto, si no se cumple $A$, entonces necesariamente se cumple $B$.

Este problema también se ve mejor con un diagrama de Hasse.