# Tablas

import java.util.Scanner;

public class ciclo {
        public static void main(String[] args) {
            int a = 1;
            while (a != 2) {
                System.out.println("Tabla de multiplicar 1 al 12");
                Scanner jv = new Scanner(System.in);
                int n;
                System.out.println("Introduce un número entero: ");
                n = jv.nextInt();
                if (n > 0 || n <= 12) {
                    System.out.println("Tabla de " + n);
                    for (int i = 1; i <= 12; i++) {
                        System.out.println(n + " * " + i + " = " + n * i);
                    }
                    System.out.println("Desea ingresar otra tabla? ");
                    System.out.println("1. Si");
                    System.out.println("2. No");
                    a = entrada.nextInt();
                }
            }
        }
}

import java.util.Scanner;
public class frase {
        public static void main(String[] args) {
            Scanner lector = new Scanner(System.in);
            String cadena = "";
            char[] Arraycadena;
            char caracter;
            int contador = 0;
            System.out.println("Escribe una frase");
            cadena = lector.nextLine();
            Arraycadena = cadena.toCharArray();
            for (int i = 0; i < Arraycadena.length; i++) {
                caracter = Arraycadena[i];
                for (int j = 0; j < Arraycadena.length; j++) {
                    if (Arraycadena[j] == caracter) {
                        contador++;
                    }
                }
                System.out.println(Arraycadena[i] + " " + contador);
                contador = 0;
            }
        }

    }
//import java.util.Scanner;
public class funciones {
        public static String saludar(String nombre)
        {
           
            String saludo = "Hola, bienvenido " + nombre;

            return saludo;//Se retorna el saludo
        }

        public static String error(String nombre)
        {
            //Se crea el mensaje de error
            String error = "Up. No pudimos validar tus datos. " + nombre + " es tu usuario?";

            return error; //Se retorna el error
        }

        public static void verificar(String usuario, String contrasenia)
        {
            String usuarioValido = "Juan";

            String contraseniaValida = "pass";

            //Se validan los datos
            if(usuarioValido.equals(usuario) && contraseniaValida.equals(contrasenia))
            {
                //Si son validos se llama ala función saludar y se muestra el mensaje retornado por pantalla
                System.out.println(saludar(usuario));
                return; //Terminamos la ejecución
            }
            //Si no son válidos entonces mostramos el mensaje de error de la funcion error.
            System.out.println(error(usuario));
        }

        public static void main(String[] args)
        {
            String usuario = "Juan";
            String contrasenia = "pass";

            //Se hace la verificación
            verificar(usuario, contrasenia);

            //Mostrará el mensaje error.
        }
    }
import java.util.Scanner;

public class arreglos {
        public static void main(String args[]) {
            int s=1;
            while(s!=2) {
                Scanner entrada = new Scanner(System.in);
                int edad[] = new int[6];
                String nombres[] = new String[6];
                String falla[] = new String[6];

                for (int x = 0; x < 6; x++) {
                    System.out.println("Ingrese nombre: ");
                    nombres[x] = entrada.nextLine();
                    System.out.println("Ingrese edad: ");
                    edad[x] = entrada.nextInt();
                    falla[x] = entrada.nextLine();
                }
                for (int y = 0; y < 6; y++) {
                    System.out.println(nombres[y] + " Cuya edad es: " + edad[y] + " annios");
                }
                System.out.println("Desea repetir?");
                System.out.println("1. Si");
                System.out.println("2. No");
                s = entrada.nextInt();
            }
        }
    }

import java.util.Scanner;
public class repaso {
        public static void main(String args[]) {
            Scanner entrada= new Scanner(System.in);
            int nota[] = new int[4];
            int nmayor = 0;
            String amayor = new String();
            String fa = new String();
            String asignaturas[] = new String[4];
            String nombre;
            String falla[] = new String[4];
            int s = 1;
            while(s!=2) {
                System.out.println("===Este programa es acerca de PROMEDIOS===");
                System.out.println("===Favor ingrese el nombre de Alumno a Promediar===");
                System.out.println("Nombre del Alumno: ");
                nombre = entrada.nextLine();
                for (int y = 0; y < 4; y++) {
                    System.out.println("Asignatura  #" + (y + 1) + ":");
                    asignaturas[y] = entrada.nextLine();
                    System.out.println("Nota #" + (y + 1) + ":");
                    nota[y] = entrada.nextInt();
                    falla[y] = entrada.nextLine();
                    if(nota[y]>nmayor){
                        nmayor=nota[y];
                        amayor= asignaturas[y];
                    }
                }
                double promedio;
                promedio=(nota[0]+nota[1]+nota[2]+nota[3])/4;
                System.out.println("Promedio del alumno:"+nombre+" es:"+promedio+"%");
                System.out.println("Su nota mas alta es en la clase: "+amayor+" con la nota de: "+nmayor+"%");
                System.out.println("Desea repetir?");
                System.out.println("1. Si");
                System.out.println("2. No");
                s = entrada.nextInt();
                fa = entrada.nextLine();
            }


        }
}
