# Lab 3 - Herencia: TecniHogar

Este proyecto contiene una aplicación sencilla de consola en Java para una empresa que realiza servicios técnicos a domicilio.

## ¿Qué puede hacer?

- Cotizar y registrar órdenes.
- Registrar cuadrillas y crear jornadas.
- Asignar y retirar órdenes.
- Iniciar jornadas y registrar si una visita fue completada o fallida.
- Mostrar reportes de órdenes, estados e ingresos.
- Validar datos incorrectos, capacidad de cuadrillas y certificación en refrigeración.

El proyecto usa herencia para representar las cuatro categorías de servicio. El UML no está incluido porque se realizará por separado.

## ¿Qué se necesita?

Se necesita tener instalado Java JDK 17 o una versión más reciente.

## ¿Cómo se ejecuta?

Desde la carpeta principal del proyecto, se ejecutan estos comandos:

```text
javac -encoding UTF-8 -d bin src\*.java
java -cp bin Main
```

La carpeta `src` contiene el código fuente, `bin` guarda los archivos compilados, `lib` queda disponible para librerías y `.vscode` contiene la configuración básica del proyecto.

El programa inicia con 8 órdenes pendientes y 3 cuadrillas de ejemplo. Los datos solo se guardan mientras el programa está abierto.

## Pruebas rápidas

1. Se elige `9` para ver las órdenes iniciales.
2. Se elige `10` y se revisa que los ingresos empiecen en Q0.00.
3. Se cotiza una instalación de 2.5 horas y 5 puntos. El resultado debe ser Q460.00.
4. Se crea una jornada con `C1`, se asignan `I1` y `A1`, y se intenta asignar `A1` a `C2`. Esa asignación debe rechazarse porque `C2` no tiene certificación en refrigeración.
5. Se inicia una jornada y se registra una visita fallida. La orden vuelve a pendiente mientras todavía tenga visitas disponibles.
