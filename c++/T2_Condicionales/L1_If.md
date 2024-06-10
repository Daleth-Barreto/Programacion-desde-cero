# Condicionales basicas
Vamos a profundizar en las estructuras de control if, if-else y if-else if-else (conocido como elif en algunos lenguajes). Estas estructuras nos permiten tomar decisiones en nuestro programa basadas en ciertas condiciones. Veamos cómo funcionan cada una de ellas en C++ y hagamos algunos ejercicios para practicarlas.
## 1. Estructura if

La estructura if ejecuta un bloque de código solo si una condición es verdadera.

``` cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numero = 10;

    if (numero > 5) { // Si la condición (numero > 5) es verdadera, ejecuta el siguiente bloque de código
        cout << "El número es mayor que 5" << endl;
    }

    return 0;
}
```

## 2. Estructura if-else

La estructura if-else ejecuta un bloque de código si una condición es verdadera y otro bloque de código si la condición es falsa.
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numero = 3;

    if (numero > 5) { // Si la condición (numero > 5) es verdadera
        cout << "El número es mayor que 5" << endl;
    } else { // Si la condición (numero > 5) es falsa
        cout << "El número no es mayor que 5" << endl;
    }

    return 0;
}
```
## 3. Estructura if-else if-else (similar a elif)

La estructura if-else if-else permite manejar múltiples condiciones. Si una condición es verdadera, se ejecuta su bloque de código correspondiente y se ignoran las demás condiciones.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numero = 7;

    if (numero > 10) { // Si la primera condición es verdadera
        cout << "El número es mayor que 10" << endl;
    } else if (numero > 5) { // Si la primera condición es falsa y la segunda es verdadera
        cout << "El número es mayor que 5 pero no mayor que 10" << endl;
    } else { // Si todas las condiciones anteriores son falsas
        cout << "El número no es mayor que 5" << endl;
    }

    return 0;
}
```
## Ejercicios
### Ejercicio 1: Comparar dos números

Escribe un programa que lea dos números del usuario y luego imprima cuál número es mayor o si son iguales.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int num1, num2;

    cout << "Introduce el primer número: ";
    cin >> num1;

    cout << "Introduce el segundo número: ";
    cin >> num2;

    if (num1 > num2) {
        cout << "El primer número (" << num1 << ") es mayor que el segundo número (" << num2 << ")." << endl;
    } else if (num1 < num2) {
        cout << "El segundo número (" << num2 << ") es mayor que el primer número (" << num1 << ")." << endl;
    } else {
        cout << "Ambos números son iguales." << endl;
    }

    return 0;
}
```
### Ejercicio 2: Calcular la calificación

Escribe un programa que lea una calificación del usuario y luego imprima si es una calificación excelente (90 o más), buena (70-89), suficiente (50-69) o insuficiente (menos de 50).

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int calificacion;

    cout << "Introduce tu calificación: ";
    cin >> calificacion;

    if (calificacion >= 90) {
        cout << "Calificación excelente" << endl;
    } else if (calificacion >= 70) {
        cout << "Calificación buena" << endl;
    } else if (calificacion >= 50) {
        cout << "Calificación suficiente" << endl;
    } else {
        cout << "Calificación insuficiente" << endl;
    }

    return 0;
}
```
### Ejercicio 3: Par o impar

Escribe un programa que lea un número del usuario y determine si el número es par o impar.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numero;

    cout << "Introduce un número: ";
    cin >> numero;

    if (numero % 2 == 0) {
        cout << "El número " << numero << " es par." << endl;
    } else {
        cout << "El número " << numero << " es impar." << endl;
    }

    return 0;
}
```
## Explicación Detallada
### Condiciones

Las condiciones en if, else if y else son expresiones que evaluamos para determinar si son verdaderas o falsas. Algunas condiciones comunes incluyen:

- Comparaciones (==, !=, <, >, <=, >=).
- Evaluación de booleanos (true o false).
- Combinaciones de condiciones usando operadores lógicos (&& para AND, || para OR, ! para NOT).

### Flujo de Ejecución

- if: Se evalúa la condición. Si es verdadera, se ejecuta el bloque de código. Si es falsa, se pasa al siguiente bloque (si existe).
- else if: Se usa después de un if para verificar otra condición si la primera fue falsa. Podemos tener múltiples else if.
- else: Se ejecuta si todas las condiciones anteriores fueron falsas. Solo puede haber un else al final de la cadena de condiciones.

## Ejemplo Completo

Vamos a ver un ejemplo completo que combina todo lo que hemos aprendido.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int edad;

    cout << "Introduce tu edad: ";
    cin >> edad;

    if (edad < 0) {
        cout << "Edad inválida. No puede ser negativa." << endl;
    } else if (edad < 13) {
        cout << "Eres un niño." << endl;
    } else if (edad < 20) {
        cout << "Eres un adolescente." << endl;
    } else if (edad < 65) {
        cout << "Eres un adulto." << endl;
    } else {
        cout << "Eres un adulto mayor." << endl;
    }

    return 0;
}
```

## Resumen

* if: Para ejecutar código basado en una condición.
* if-else: Para manejar dos posibles caminos (verdadero o falso).
* if-else if-else: Para manejar múltiples condiciones.

Practica estos conceptos escribiendo tus propios programas. Cuanto más practiques, más cómodo te sentirás usando estas estructuras de control en tus programas.