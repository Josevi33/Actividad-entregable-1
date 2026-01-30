# Analizador de Números 
 
Proyecto de refactorización en Java para la asignatura de Entornos de Desarrollo. 
 
## Funcionalidad 
- Obtiene el valor máximo de un array 
- Comprueba si el máximo se repite 
- Calcula la media 
- Evalúa si la media es suficiente 
 
## Tecnologías utilizadas
- Java 
- Git / GitHub 

### Código fuente del programa

```java
package ejercicios;

/** 
 * Clase que analiza un array de números: 
 * - Comprueba si el valor máximo se repite 
 * - Calcula la media 
 * - Evalúa si la media es suficiente 
 * 
 * @author Jose Vicente Ros Campos 
 * @version 1.0 
 */
public class AnalizadorNumeros {

    public static void main(String[] args) {

        int[] numeros = {5, 7, 3, 7, 2, 9, 7};

        int maximo = obtenerMaximo(numeros);
        boolean maximoRepetido = estaRepetido(numeros, maximo);

        System.out.println(maximoRepetido ? "SI" : "NO");

        double media = calcularMedia(numeros);
        System.out.println(media);

        System.out.println(media >= 5 ? "BIEN" : "MAL");
    }

    public static int obtenerMaximo(int[] numeros) {
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        return maximo;
    }

    public static boolean estaRepetido(int[] numeros, int valor) {
        int contador = 0;
        for (int numero : numeros) {
            if (numero == valor) {
                contador++;
            }
        }
        return contador > 1;
    }

    public static double calcularMedia(int[] numeros) {
        int suma = 0;
        for (int numero : numeros) {
            suma += numero;
        }
        return (double) suma / numeros.length;
    }
}
 
## Autor 
Jose Vicente Ros Campos

