# Colecciones

## ¿Qué es una coleccion en Java?

Una colección es un contenedor para un conjunto de elementos de un tipo.

## Framework de colecciones de Java

-Intefarces: tipos de datos, independientes de su representacion
-Implementaciones: concreciones de los diferentes tipos
-Algoritmos: metodos para buscar, ordenar, clasificar.

## Ventajas del framework

- Reduce el esfuerzo de progrmación
- Aumenta la calidad y velocidad del programa
- Fomenta la reutalización
- Facilita el aprendizaje tanto de uso como de diseño de librerias

## Tipos de colecciones

### Iterable<E>
	
Concepto de Iretador: 
	- Patrón de diseño
	- Recorrer y eliminar los elementos
Permite usar forEach y el bucle tipo for-each

### Collection<E>

- Extiende a iterable
- Representa un grupo de elementos
- Sirve para manipular colecciones de manera general

#### Operaciones de Collection

- tamaño (size, isEmpty)
- comprobacion (contains)
- Iterar (iterator)
- Operaciones bulk (containsAll, addAll, removeall, removeIf, retainAll, clear)
- Añadir y eliminar (add, remove)
- transformar a array (toArray)
- Strams (stream, parallelStream)

### Set<E>

- No permite elementos duplicados
- No hay acceso posicional (por ejemplo no se puede acceder al tercer elemento)
- Mejora la implementación de equals y hashCode

#### Implementaciones de Set<E>

- HashSet<E> - Más rapida
- LinkedHashSet<E> - Orden de inserción
- TreeSet<E> - Orden según su valor

### List<E>

- Permite duplicados
- Se añaden las siguientes funciones:
	- Acceso posicinal
	- Busqueda
	- Iteración extendida
	- Operaciones sobre un rango de elementos de la lista

### Queue <E>

- Funciona como una cola FIFO
- Funciones lanzan excepcion: (add, remove, element)
- Funciones devuelven nulo: (offer, poll, peek)

### Deque <E>

- Puede funcionar como cola o como una pila
- Puede funcionar como pila doble

### Map<K,V>

- No hereda de Collection<E>
- Maneja pares clave, valor
- Para cada clave solo hay un valor
- Cada clave puede existir una sola vez en el map
- Puede haber un clave nula, y multiples valores nulos
- Se le conoce también como diccionario
- No puede almacenar tipos primitivos (int -> Integer)

#### Map.Entry<K,V>

- Permite consultar un par clave,valor
- No se puede usar para insertar valores

#### Implementaciones de Map<K,V>

- HashMap<K,V> - Más rapida
- LinkedHashMap<K,V> - Orden de inserción
- TreeMap<K,V> - Orden según su valor

### Colecciones no modificables

Son colecciones que una vez creadas no se pueden cambiar. Un uso para
estas podría ser como resultado de una operación.

### Colecciones sincronizadas

Aptas para el uso de diferentes hilos de ejecución.
Varios procesos que compiten por e uso de la colección

## Algoritmos

### Ordenacion

Collections.sort(lista)
	- Recibe una colección, modifica la colección recibida
	- Los elementos deben implementar Comparable
	
Collections.sort(lista, comparador)
	- Ordena según el orden inducido por el comparador

### Desordenación

Collections.shuffle(lista)
	- Lo contrario que sort
	
Collections.shuffle(lista, random)
	- Se le proporciona el componente aleatorio

### Busqueda
	
- Busqueda binaria
- La lista debe estar ordenada previamente
- Si se repite un valor no se sabe cual va a encontrarse
- Si lo encuentra nos da el indice

### Algunas operaciones
	
Máximo y minimo
	- Acorde al orden natural, se puede implementar con Comparator
Frecuencia
	- Devuelve el número de veces que aparece un objeto
