# Estructura Básica de un Programa en C++

Cada programa en C++ comienza con #include <bits/stdc++.h> y una función llamada main. Todo el código que queremos que se ejecute se coloca dentro de esta función. Aquí tienes el programa más simple en C++:

```cpp

#include <bits/stdc++.h> // Incluye muchas librerías útiles
using namespace std; // Evita tener que escribir std:: antes de cada cosa de la librería estándar

int main() {
    cout << "¡Hola, Mundo!" << endl; // Imprime "¡Hola, Mundo!" en la pantalla
    return 0; // Indica que el programa terminó correctamente
}
```
## Vamos a desglosar esto:

* #include <bits/stdc++.h>: Esto incluye muchas librerías útiles de C++.
* using namespace std;: Esto nos permite usar nombres de la biblioteca estándar de C++ sin tener que escribir std:: antes de ellos.
* int main() { ... }: Esta es la función principal de nuestro programa. Todo el código que queremos ejecutar va dentro de estas llaves {}.
* cout << "¡Hola, Mundo!" << endl;: Esto imprime el texto "¡Hola, Mundo!" en la pantalla, "endl" da un salto de linea como "\n"
* return 0;: Esto indica que el programa terminó correctamente.
