# Switch
Vamos a aprender sobre la estructura switch en C++, que es otra forma de tomar decisiones en tu programa. La estructura switch es especialmente útil cuando tienes múltiples condiciones que dependen del valor de una sola variable. Vamos a ver cómo funciona.

## Estructura del switch

La estructura switch permite ejecutar diferentes partes del código según el valor de una expresión, típicamente una variable. Aquí está la sintaxis básica:

```cpp

switch (expresion) {
    case valor1:
        // Código a ejecutar si expresion == valor1
        break;
    case valor2:
        // Código a ejecutar si expresion == valor2
        break;
    // Puedes tener tantos casos como necesites
    default:
        // Código a ejecutar si ninguno de los casos anteriores coincide
}
```
## Desglose de la Estructura

- expresion: Es una variable o expresión cuyo valor se va a comparar con los diferentes casos.
- case valor1, case valor2, ...: Cada uno de estos es un caso que compara la expresión con un valor específico. Si la expresión coincide con el valor, se ejecuta el código correspondiente.
- break: Termina la ejecución del switch y evita que el programa siga ejecutando el siguiente caso. Sin break, se ejecutarán todos los casos siguientes hasta encontrar un break o el final del switch.
- default: Es opcional y se ejecuta si ninguno de los casos coincide. Funciona como un "catch-all".

## Ejemplo Básico

Vamos a ver un ejemplo donde usamos switch para imprimir el nombre de un día de la semana según un número dado:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int dia;

    cout << "Introduce un número del 1 al 7: ";
    cin >> dia;

    switch (dia) {
        case 1:
            cout << "Lunes" << endl;
            break;
        case 2:
            cout << "Martes" << endl;
            break;
        case 3:
            cout << "Miércoles" << endl;
            break;
        case 4:
            cout << "Jueves" << endl;
            break;
        case 5:
            cout << "Viernes" << endl;
            break;
        case 6:
            cout << "Sábado" << endl;
            break;
        case 7:
            cout << "Domingo" << endl;
            break;
        default:
            cout << "Número inválido" << endl;
    }

    return 0;
}
```
## Detalles Importantes

    Tipos de Datos: La expresión en un switch generalmente es de tipo int o char. Otros tipos de datos pueden funcionar, pero es menos común.
    Uso de break: Es crucial incluir break después de cada caso para evitar la "caída" a través de los casos siguientes. Sin break, todos los casos debajo del coincidente también se ejecutarán.
    default Opcional: Aunque opcional, es una buena práctica incluirlo para manejar valores imprevistos.

## Ejercicios

Vamos a practicar un poco con switch.
### Ejercicio 1: Menú de Opciones

Escribe un programa que muestre un menú con 3 opciones y lea la selección del usuario. Según la opción seleccionada, debe imprimir un mensaje diferente.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int opcion;

    cout << "Menú de opciones:" << endl;
    cout << "1. Saludar" << endl;
    cout << "2. Despedirse" << endl;
    cout << "3. Mostrar agradecimiento" << endl;
    cout << "Introduce tu opción (1-3): ";
    cin >> opcion;

    switch (opcion) {
        case 1:
            cout << "¡Hola, usuario!" << endl;
            break;
        case 2:
            cout << "Adiós, hasta luego." << endl;
            break;
        case 3:
            cout << "¡Gracias por usar nuestro programa!" << endl;
            break;
        default:
            cout << "Opción inválida" << endl;
    }

    return 0;
}
```
### Ejercicio 2: Conversión de Notas

Escribe un programa que convierta una calificación numérica a una letra según la siguiente tabla:

* 90-100: A
* 80-89: B
* 70-79: C
* 60-69: D
* Menos de 60: F

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int nota;

    cout << "Introduce la calificación (0-100): ";
    cin >> nota;

    switch (nota / 10) { // Dividimos por 10 para simplificar el uso del switch
        case 10:
        case 9:
            cout << "Calificación: A" << endl;
            break;
        case 8:
            cout << "Calificación: B" << endl;
            break;
        case 7:
            cout << "Calificación: C" << endl;
            break;
        case 6:
            cout << "Calificación: D" << endl;
            break;
        default:
            cout << "Calificación: F" << endl;
    }

    return 0;
}
```
## Extra

En C++, el switch es bastante estándar y no tiene muchas variantes. Sin embargo, hay algunas consideraciones y prácticas que pueden variar:

- Agrupación de Casos: Puedes agrupar varios casos que tengan la misma salida.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    char letra;

    cout << "Introduce una letra (a, e, i, o, u): ";
    cin >> letra;

    switch (letra) {
        case 'a':
        case 'e':
        case 'i':
        case 'o':
        case 'u':
            cout << "Es una vocal." << endl;
            break;
        default:
            cout << "No es una vocal." << endl;
    }

    return 0;
}
```
- Fallthrough Intencional: A veces es útil dejar que la ejecución "caiga" a través de varios casos sin break. Esto puede ser útil en ciertas situaciones, pero debe usarse con cuidado.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int mes;

    cout << "Introduce el número del mes (1-12): ";
    cin >> mes;

    switch (mes) {
        case 12:
        case 1:
        case 2:
            cout << "Es invierno." << endl;
            break;
        case 3:
        case 4:
        case 5:
            cout << "Es primavera." << endl;
            break;
        case 6:
        case 7:
        case 8:
            cout << "Es verano." << endl;
            break;
        case 9:
        case 10:
        case 11:
            cout << "Es otoño." << endl;
            break;
        default:
            cout << "Número de mes inválido" << endl;
    }

    return 0;
}
```