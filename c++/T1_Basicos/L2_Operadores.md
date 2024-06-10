# Operadores
Los operadores son símbolos que nos permiten realizar operaciones en nuestros datos. Pueden ser aritméticos, de comparación, lógicos, de asignación, bit a bit, y más. Vamos a ver cada tipo con ejemplos detallados.
## 1. Operadores Aritméticos

Los operadores aritméticos nos permiten realizar operaciones matemáticas básicas.

    Suma (+): Añade dos valores.
    Resta (-): Resta el segundo valor del primero.
    Multiplicación (*): Multiplica dos valores.
    División (/): Divide el primer valor por el segundo.
    Módulo (%): Devuelve el resto de la división del primer valor por el segundo (solo para enteros).

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int a = 10, b = 3;
    cout << "a + b = " << (a + b) << endl; // Suma
    cout << "a - b = " << (a - b) << endl; // Resta
    cout << "a * b = " << (a * b) << endl; // Multiplicación
    cout << "a / b = " << (a / b) << endl; // División
    cout << "a % b = " << (a % b) << endl; // Módulo

    return 0;
}
```
## 2. Operadores de Asignación

Los operadores de asignación se usan para asignar valores a las variables.

* Asignación (=): Asigna el valor de la derecha a la variable de la izquierda.
* Asignación con suma (+=): Suma el valor de la derecha a la variable de la izquierda y asigna el resultado a la variable de la izquierda.
* Asignación con resta (-=): Resta el valor de la derecha a la variable de la izquierda y asigna el resultado a la variable de la izquierda.
* Asignación con multiplicación (*=): Multiplica el valor de la derecha con la variable de la izquierda y asigna el resultado a la variable de la izquierda.
* Asignación con división (/=): Divide la variable de la izquierda por el valor de la derecha y asigna el resultado a la variable de la izquierda.
* Asignación con módulo (%=): Realiza el módulo de la variable de la izquierda con el valor de la derecha y asigna el resultado a la variable de la izquierda.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int a = 10;

    a += 5; // a = a + 5
    cout << "a += 5: " << a << endl;

    a -= 3; // a = a - 3
    cout << "a -= 3: " << a << endl;

    a *= 2; // a = a * 2
    cout << "a *= 2: " << a << endl;

    a /= 4; // a = a / 4
    cout << "a /= 4: " << a << endl;

    a %= 3; // a = a % 3
    cout << "a %= 3: " << a << endl;

    return 0;
}
```
## 3. Operadores de Comparación

Los operadores de comparación nos permiten comparar dos valores. El resultado de estas comparaciones es un valor booleano (true o false).

* Igual a (==): Verifica si dos valores son iguales.
* Diferente de (!=): Verifica si dos valores son diferentes.
* Menor que (<): Verifica si el valor de la izquierda es menor que el valor de la derecha.
* Mayor que (>): Verifica si el valor de la izquierda es mayor que el valor de la derecha.
* Menor o igual que (<=): Verifica si el valor de la izquierda es menor o igual que el valor de la derecha.
* Mayor o igual que (>=): Verifica si el valor de la izquierda es mayor o igual que el valor de la derecha.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int x = 5, y = 10;

    cout << "x == y: " << (x == y) << endl; // Igual a
    cout << "x != y: " << (x != y) << endl; // Diferente de
    cout << "x < y: " << (x < y) << endl; // Menor que
    cout << "x > y: " << (x > y) << endl; // Mayor que
    cout << "x <= y: " << (x <= y) << endl; // Menor o igual que
    cout << "x >= y: " << (x >= y) << endl; // Mayor o igual que

    return 0;
}
```
## 4. Operadores Lógicos

Los operadores lógicos se usan para combinar expresiones lógicas y devuelven un valor booleano.

* AND lógico (&&): Devuelve true si ambas expresiones son verdaderas.
* OR lógico (||): Devuelve true si al menos una de las expresiones es verdadera.
* NOT lógico (!): Invierte el valor lógico de una expresión.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    bool a = true, b = false;

    cout << "a && b: " << (a && b) << endl; // AND lógico
    cout << "a || b: " << (a || b) << endl; // OR lógico
    cout << "!a: " << (!a) << endl; // NOT lógico

    return 0;
}
```
## 5. Operadores de Incremento y Decremento

Los operadores de incremento y decremento se usan para aumentar o disminuir el valor de una variable en uno.

* Incremento (++): Aumenta el valor de la variable en uno.
* Decremento (--): Disminuye el valor de la variable en uno.

Estos operadores pueden ser prefijos (antes de la variable) o sufijos (después de la variable).

* Prefijo (++a, --a): Incrementa o decrementa la variable antes de usar su valor.
* Sufijo (a++, a--): Usa el valor actual de la variable antes de incrementar o decrementar.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int x = 10;

    cout << "x++: " << (x++) << endl; // Sufijo: usa el valor de x, luego incrementa
    cout << "Después de x++: " << x << endl;

    cout << "++x: " << (++x) << endl; // Prefijo: incrementa, luego usa el valor de x

    cout << "x--: " << (x--) << endl; // Sufijo: usa el valor de x, luego decrementa
    cout << "Después de x--: " << x << endl;

    cout << "--x: " << (--x) << endl; // Prefijo: decrementa, luego usa el valor de x

    return 0;
}
```
**Nota:** Ya has visto lo escencial, el resto es complejo
## 6. Operadores Bit a Bit

Los operadores bit a bit trabajan directamente con los bits de los números.

* AND bit a bit (&): Compara cada bit de dos números y devuelve 1 solo si ambos bits son 1.
* OR bit a bit (|): Compara cada bit de dos números y devuelve 1 si al menos uno de los bits es 1.
* XOR bit a bit (^): Compara cada bit de dos números y devuelve 1 si uno de los bits es 1 y el otro es 0.
* NOT bit a bit (~): Invierte todos los bits de un número.
* Desplazamiento a la izquierda (<<): Desplaza los bits de un número a la izquierda.
* Desplazamiento a la derecha (>>): Desplaza los bits de un número a la derecha.

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int a = 5, b = 3; // 5 es 0101 en binario, 3 es 0011 en binario

    cout << "a & b: " << (a & b) << endl; // AND bit a bit: 0001 (1)
    cout << "a | b: " << (a | b) << endl; // OR bit a bit: 0111 (7)
    cout << "a ^ b: " << (a ^ b) << endl; // XOR bit a bit: 0110 (6)
    cout << "~a: " << (~a) << endl; // NOT bit a bit: 1010 en complemento a dos (-6)
    cout << "a << 1: " << (a << 1) << endl; // Desplazamiento a la izquierda: 1010 (10)
    cout << "a >> 1: " << (a >> 1) << endl; // Desplazamiento a la derecha: 0010 (2)

    return 0;
}
```
## 7. Operadores de Miembro de Puntero

Estos operadores se utilizan con punteros para acceder a miembros de estructuras o clases.

* Operador de acceso a miembro de puntero (->): Se usa para acceder a un miembro de una estructura o clase a través de un puntero.
* Operador de referencia de miembro (.*): Se usa para acceder a un miembro de una estructura o clase a través de un puntero a miembro.

```cpp

#include <bits/stdc++.h>
using namespace std;

struct Punto {
    int x, y;
};

int main() {
    Punto p = {1, 2};
    Punto* ptr = &p;

    cout << "p.x: " << p.x << endl; // Acceso directo
    cout << "ptr->x: " << ptr->x << endl; // Acceso a través de puntero

    return 0;
}
```
