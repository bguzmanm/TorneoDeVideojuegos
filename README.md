# Descripción del Problema

Imagina que eres el organizador de un torneo de videojuegos. Necesitas desarrollar un programa en Java para gestionar los equipos participantes, los jugadores de cada equipo y los resultados de los partidos. Los equipos pueden inscribirse al torneo, agregar jugadores a sus equipos y registrar los resultados de los partidos. Al final, el programa debe ser capaz de mostrar un ranking de los equipos basado en los resultados de los partidos.

## Requisitos Específicos

1. **Gestión de Equipos y Jugadores:**
    1. Cada equipo tiene un nombre único y una lista de jugadores.
    2. Cada jugador tiene un nombre y un alias.
    3. Se debe permitir agregar nuevos equipos.
    4. Se debe permitir agregar jugadores a un equipo específico.
2. **Registro de Partidos:**
    1. Cada partido se juega entre dos equipos.
    2. Debes registrar los resultados de cada partido indicando qué equipo ganó.
3. **Ranking de Equipos:**
    1. Cada equipo obtiene 3 puntos por una victoria, 1 para el empate y 0 puntos por una derrota.
    2. El programa debe ser capaz de mostrar el ranking de los equipos basado en los puntos acumulados.
4. **Colecciones Sugeridas:**
    1. Usa ArrayList para gestionar la lista de jugadores de cada equipo.
    2. Usa HashMap para gestionar los equipos, donde la clave es el nombre del equipo y el valor es el objeto equipo que contiene la lista de jugadores y sus puntos.
    3. Usa ArrayList para gestionar los resultados de los partidos.

## Clase Principal y Estructuras de Datos:

Define las siguientes clases para ayudarte a organizar el código:

1. **Clase Jugador:**
    1. Atributos: nombre, alias.
    2. Métodos: constructor, getters y setters.
2. **Clase Equipo:**
    1. Atributos: nombre, lista de jugadores (ArrayList<Jugador>), puntos.
    2. Métodos: constructor, métodos para agregar jugadores, getters y setters.
3. **Clase Torneo:**
    1. Atributos: equipos (HashMap<String, Equipo>), resultados de partidos (ArrayList<String>).
    2. Métodos: métodos para agregar equipos, agregar jugadores a equipos, registrar resultados de partidos, mostrar ranking de equipos.

# Ejemplo de Interacción

```java
public class TorneoDeVideojuegos {
    public static void main(String[] args) {
        Torneo torneo = new Torneo();

        // Agregar equipos
        torneo.agregarEquipo("Equipo Alpha");
        torneo.agregarEquipo("Equipo Beta");

        // Agregar jugadores a los equipos
        torneo.agregarJugador("Equipo Alpha", new Jugador("Alice", "Alicia2000"));
        torneo.agregarJugador("Equipo Alpha", new Jugador("Bob", "Bobster"));
        torneo.agregarJugador("Equipo Beta", new Jugador("Charlie", "Chaz"));

        // Registrar resultados de partidos
        torneo.registrarResultado("Equipo Alpha", "Equipo Beta", "Equipo Alpha");

        // Mostrar ranking
        torneo.mostrarRanking();
    }
}
```