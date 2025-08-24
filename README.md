# Laboratorio 01 - Introducción a Prolog  

## 📌 Descripción  
Este laboratorio tiene como objetivo que los estudiantes fortalezcan sus conocimientos iniciales en **Prolog**, abordando temas como:  
- Hechos y consultas simples  
- Definición de reglas  
- Predicados con condiciones aritméticas
- Recursión simple (definición por casos)
- Listas

El desarrollo se realizará en **[SWISH Prolog](https://swish.swi-prolog.org/)**, un entorno en línea que no requiere instalación local.  

---

## 🛠️ Instrucciones Generales  

1. **Fork del repositorio**  
   - Realice un **fork** de este repositorio en su cuenta personal de GitHub.  
   - No realice cambios directamente sobre el repositorio original.  

2. **Estructura de carpetas**  
   - Dentro de su fork, cree una carpeta llamada **`lab01/`**.  
   - Cada ejercicio debe resolverse en un archivo **independiente** con el siguiente formato:  
     ```
     lab01/ejercicio01.pl
     lab01/ejercicio02.pl
     ...
     ```  

3. **Resolución de ejercicios**  
   - Desarrolle los programas en **SWISH Prolog**.  
   - Una vez finalizados, copie el código a los archivos `.pl` correspondientes en su repositorio.  
   - Cada archivo debe contener:
     - La implementación de su solución.  

4. **Buenas prácticas**  
   - Use **nombres de predicados claros y significativos**.
---

## 🚀 Entrega  

- **Plazo**: La entrega debe realizarse a mas tardar el proximo lunes, se habilitara una tarea en Moodle para adjuntar el link del repositorio.

---

## ✅ Criterios de Evaluación  

1. **Correctitud de las soluciones** (funcionalidad de los predicados).  
2. **Cumplimiento de la estructura solicitada** (archivos independientes en `lab01/`).  
3. **Claridad en la codificación** (nombres, comentarios y legibilidad).  
4. **Uso adecuado de variables** (incluyendo variables anónimas donde corresponda).  

---

## 💡 Recomendaciones  

- Revise la documentación oficial de Prolog: [SWI-Prolog Documentation](https://www.swi-prolog.org/pldoc/).  
- Antes de subir sus archivos, **ejecute y verifique** cada consulta en SWISH.  
- Mantenga su repositorio organizado y actualizado.

---

## Ejercicio 1 - Hechos y consultas simples

Dada la siguiente base de conocimiento
```
% Hechos: relación entre ciudades
ciudad(bogota).
ciudad(medellin).
ciudad(cali).
ciudad(cartagena).
ciudad(manizales).
ciudad(barranquilla).
ciudad(pasto).
ciudad(monteria).

% Hechos: vuelos directos
vuelo(bogota, medellin).
vuelo(medellin, cartagena).
vuelo(cali, bogota).
vuelo(bogota, cartagena).
vuelo(manizales, cartagena).
vuelo(medellin, barranquilla).
vuelo(pasto, bogota).
vuelo(bogota, pasto).

```

Responde:

1. ¿Existe un vuelo directo de Bogotá a Medellín?.
2. ¿Qué destinos se pueden alcanzar directamente desde Bogotá?.
3. ¿Desde que destinos se puede alcanzar Medellin?
4. ¿Hay alguna forma de llegar directamente a cali?

## Ejercicio 2 - Reglas basicas

Dada la base de conocimiento de vuelos, define una regla que:

- Determine si dos ciudades están conectadas mediante una escala.
     - Ahora, verifica si existe una conexión de Bogotá a Barranquilla.
- Encuentra todas las ciudades a las que se puede llegar desde Cali con una escala.
- Define una regla viaje que sea cierta si existe un vuelo directo o con una escala entre dos ciudades (no usar recursion).
   - Ahora, verifica si existe un viaje posible de Bogotá a Pasto.

- Define una regla destinos que devuelva la lista de todos los destinos alcanzables directamente desde una ciudad.

---

Dada la base de conocimiento.

```
perro(firulais).
perro(bruno).
perro(max).
gato(misu).
gato(luna).
gato(chanel).
gato(orion).
ave(piolin).

dueno(ana, firulais).
dueno(ana, misu).
dueno(luis, luna).
dueno(luis, orion).
dueno(luis, firulais).
dueno(maria, piolin).
dueno(julia, chanel).
dueno(pedro, bruno).
```

Responde:

- Define una regla que determine si una persona tiene un perro.
   - Ahora, encuentra los dueños de perros.
- Define una regla que determine si una persona tiene un gato.
   - Ahora, encuentra los dueños de gatos.
- Define una regla que determine si una persona tiene multiples mascotas.
   - Ahora, encuentra los dueños de multiple tipos de mascota.
- Define una regla amante_animales para identificar dueños que tienen tanto perro como gato.
- Define una regla mascota_compartida que indique si dos personas comparten mascota.
- Define una regla tipo_mascota que asocie una persona con el tipo de mascota que tiene (perro, gato, ave, etc.).

