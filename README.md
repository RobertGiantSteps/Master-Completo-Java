
![desktop-wallpaper-java-programming](https://github.com/RobertGiantSteps/Master-Completo-Java/assets/91851811/98da4622-005d-43bb-b708-44033b1fdb4f)

# Master Completo Java IntelliJ

[Java_Programming_Masterclass_17](https://www.notion.so/Java_Programming_Masterclass_17-7975cfb986f3416b9b75bafedbc81a4c?pvs=21)

Para abrir **IntelliJ** desde el terminal de Mac

![Captura de Pantalla 2023-09-25 a las 5.14.33.png](Master%20Completo%20Java%20IntelliJ%2037f662702e6a4fb58b89cd6f550bc10a/Captura_de_Pantalla_2023-09-25_a_las_5.14.33.png)

**Atajos:**

**p**(public)**s**(static)**v**(void)**m**(main) + **Tab** (Método main) o **main** **+ Tab**

**s**(System)**o**(out)**ut + Tab (System.out.println)**

**s**(System)**o**(out)**utv + Tab (System.out.println(imprime la  variable definida previamente del programa);)**

---

<aside>
👉🏼 Java tiene 2 tipos de datos a modo general los **Primitivos** (solo un valor ) y los de **Referencia**(Objetos, instancias de una clase).

</aside>

---

Ejemplos de Variables en Java

```java
public class HolaMundo {
    public static void main(String[] args) {

        // Tipo String es un objeto por eso tiene métodos:
        
        String greeting = "Hola mundo desde Java";
        System.out.println(greeting);
        System.out.println("greeting con Mayúsculas = " + greeting.toUpperCase());

        // Tipo Primitivo int

        int number = 10;

        System.out.println("number = " + number);
        System.out.println("El tipo de dato int tiene un rango de (" + Integer.MIN_VALUE + " hasta " + Integer.MAX_VALUE + ")");

        // Con var tenemos inferncia de tipo no hace falta declara el tipo de la variable esta es dinámica según el literal que es el valor
        var flexibleVariable = 15;

        System.out.println("flexibleVariable = " + flexibleVariable);

    }
}
```

**Reglas Básicas en Java para la creación de variables** 

1. Una variable puede ser definida sin un valor ⇒⇒>   **String name**;
2. El valor se puede asignar después.                               **name = “Bob”;**
3. Los nombres de variables no pueden ser palabra reservada por el lenguaje

![PalabrasReservadas.PNG](Master%20Completo%20Java%20IntelliJ%2037f662702e6a4fb58b89cd6f550bc10a/PalabrasReservadas.png)

4.**Las variables no pueden empezar por un número**

1. Por convención los nombres de variables con palabras compuestas **seSeparanConMayúsculas** (cammel case)
2. No se recomienda usar tildes ´ o ñ.  

Los comentarios en Java de una sola línea con **//**

Los comentarios multilíneas **/**/**

---

### **Primitivos en Java**

[1_variables.pdf](Master%20Completo%20Java%20IntelliJ%2037f662702e6a4fb58b89cd6f550bc10a/1_variables.pdf)

[Datos Primitivos .pdf](Master%20Completo%20Java%20IntelliJ%2037f662702e6a4fb58b89cd6f550bc10a/1_primitivos.pdf)

Datos Primitivos .pdf

![primitivos.jpg](Master%20Completo%20Java%20IntelliJ%2037f662702e6a4fb58b89cd6f550bc10a/primitivos.jpg)

<aside>
👉🏼 Entre los números reales (**float,double**), uno es de precisión simple y otro de precisión doble

</aside>

<aside>
👉🏼 En el caso de los char corresponde a un solo caracter, se escribe con **comillas simples ‘ ‘, puede ser más de un carácter cuando se usa código UNICODE y ocupa cada carácter 16 bits.**

</aside>

```java
char a = 'a';
char b = '1';
char c = '\u0021';
```

![secuencias de escape.png](Master%20Completo%20Java%20IntelliJ%2037f662702e6a4fb58b89cd6f550bc10a/secuencias_de_escape.png)

<aside>
👀 La literal de un **long (el valor) será tomado como integer por defecto para que sea tratado como un long debemos colocar al final del número la letra ‘L’**

</aside>

<aside>
👀 En el caso de colocar con **var** una literal numérica esta será tomada por defecto como Integer si nos pasamos de su rango máximo tendremos que colocarle la **‘L’** para que sea tratado como long

</aside>

```java
public class Primitivos {
    public static void main(String[] args) {

        // byte -128 a 127
        byte byteNumber = 7;
        System.out.println("byteNumber = " + byteNumber);
        System.out.println("El tipo byte corresponde en byte = " + Byte.BYTES);
        System.out.println("El tipo byte corresponde en bits = " + Byte.SIZE);
        System.out.println("El valor máximo de rango es " + Byte.MAX_VALUE+ " y el mínimo a " + Byte.MIN_VALUE);

        System.out.println();

        // short -32.768 a 32.767
        short shortNumber = 30000;
        System.out.println("El tipo short corresponde en byte = " + Short.BYTES);
        System.out.println("El tipo short corresponde en bits = " + Short.SIZE);
        System.out.println("El valor máximo de rango es " + Short.MAX_VALUE+ " y el mínimo a " + Short.MIN_VALUE);

        System.out.println();

        // int -2147483648 a 2147483647
        int intNumber = 32758;
        System.out.println("El tipo int corresponde en byte = " + Integer.BYTES);
        System.out.println("El tipo int corresponde en bits = " + Integer.SIZE);
        System.out.println("El valor máximo de rango es " + Integer.MAX_VALUE+ " y el mínimo a " + Integer.MIN_VALUE);

        System.out.println();

        // long -9223372036854775808 a 9223372036854775807
        long longNumber = 2147483648L; //OJO Para especificar que la literal (el valor) es un long con la 'L'
        System.out.println("El tipo long corresponde en byte = " + Long.BYTES);
        System.out.println("El tipo long corresponde en bits = " + Long.SIZE);
        System.out.println("El valor máximo de rango es " + Long.MAX_VALUE+ " y el mínimo a " + Long.MIN_VALUE);

        System.out.println();

        // var(si se le asigna ala literal un número lo va a tomar como integer no como byte, short etc ...)
        /* Si el número asignado a la literal de var se pasa del rango de un Integer
        * Tenemos que colocarle el sufijo 'L' para que lo trate como long*/
        var varNumber = 9223372036854775807L ;

    }
}
```

```bash
byteNumber = 7
El tipo byte corresponde en byte = 1
El tipo byte corresponde en bits = 8
El valor máximo de rango es 127 y el mínimo a -128

El tipo short corresponde en byte = 2
El tipo short corresponde en bits = 16
El valor máximo de rango es 32767 y el mínimo a -32768

El tipo int corresponde en byte = 4
El tipo int corresponde en bits = 32
El valor máximo de rango es 2147483647 y el mínimo a -2147483648

El tipo long corresponde en byte = 8
El tipo long corresponde en bits = 64
El valor máximo de rango es 9223372036854775807 y el mínimo a -9223372036854775808

Process finished with exit code 0
```

### Primitivos tipo float - double

```java
public class PrimitivosFloatDouble {
    public static void main(String[] args) {

        // float desde 1.4E-45 a 3.4028235E38
        /* Si a esta literal le colocáramos el 1.0 nos daría un error
        * ,pues automáticamente Java lo trata como double y no se puede asignar un double a un float
        * para ello tendríamos que colocar la 'f' 1.0f en la literal para que sea tratado como float este valor
        * Noteción Científica Ejemplo 1.5e4 = (1.5 * 10 ^ 4) = 15000.0 si el exponente es negativo 1.5e-4
        * se corre el punto a la izquierda 0.00015 */

        float realFloat = 2.12e3f; // Es lo mismo que escribir 2120f e(exponente * 10 ^ 3) se corre el punto 3 veces a la derecha 2120.0 ;
        System.out.println("realFloat = " + realFloat);
        System.out.println("El tipo float corresponde en byte = " + Float.BYTES);
        System.out.println("El tipo float corresponde en bits = " + Float.SIZE);
        System.out.println("El valor máximo de rango es " + Float.MAX_VALUE+ " y el mínimo a " + Float.MIN_VALUE);

				 System.out.println();

        // double desde 4.9E-324 a 1.7976931348623157E308
        double realDouble = 3.4028235E38;
        System.out.println("realDouble = " + realDouble);
        System.out.println("El tipo double corresponde en byte = " + Double.BYTES);
        System.out.println("El tipo double corresponde en bits = " + Double.SIZE);
        System.out.println("El valor máximo de rango es " + Double.MAX_VALUE+ " y el mínimo a " + Double.MIN_VALUE);

				 
System.out.println();
        
        // var dinámica (Por defecto si tiene punto decimal es tratado como double si queremos que se afloat tenemos que agregar la 'f')
        /* Si quitamos el punto flotante a este ejemplo sería tomado como integer por defecto */
        var varFloat = 3.1416;
        System.out.println("varFloat = " + varFloat);
    }
}
```
