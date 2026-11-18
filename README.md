using System;

namespace Tarea2
{
    class Program
    {
        // funcion 1: area del triangulo
        static double AreaTriangulo(double base1, double altura)
        {
            double area;
            area = (base1 * altura) / 2;
            return area;
        }

        // funcion 2: area del cuadrado
        static double AreaCuadrado(double lado)
        {
            double area;
            area = lado * lado;
            return area;
        }

        // funcion 3: area del circulo
        static double AreaCirculo(double radio)
        {
            double area;
            area = 3.14 * radio * radio;
            return area;
        }

        // funcion 4: mayor o menor de edad
        static string MensajeEdad(int edad)
        {
            string mensaje;

            if (edad >= 18)
            {
                mensaje = "La persona es mayor de edad";
            }
            else
            {
                mensaje = "La persona es menor de edad";
            }

            return mensaje;
        }

        static void Main(string[] args)
        {
            double base1, altura, lado, radio;
            double areaTriangulo, areaCuadrado, areaCirculo;
            int edad;

            Console.WriteLine("========================================");
            Console.WriteLine("  TAREA 2 - AREAS Y MAYORIA DE EDAD");
            Console.WriteLine("========================================");
            Console.WriteLine();

            // triangulo (ejemplo: base 10, altura 5 = 25)
            Console.WriteLine("AREA DEL TRIANGULO");
            Console.Write("Digite la base: ");
            base1 = Convert.ToDouble(Console.ReadLine());
            Console.Write("Digite la altura: ");
            altura = Convert.ToDouble(Console.ReadLine());
            areaTriangulo = AreaTriangulo(base1, altura);
            Console.WriteLine("El area del triangulo es: " + areaTriangulo);
            Console.WriteLine();

            // cuadrado (ejemplo: lado 4 = 16)
            Console.WriteLine("AREA DEL CUADRADO");
            Console.Write("Digite el lado: ");
            lado = Convert.ToDouble(Console.ReadLine());
            areaCuadrado = AreaCuadrado(lado);
            Console.WriteLine("El area del cuadrado es: " + areaCuadrado);
            Console.WriteLine();

            // circulo (ejemplo: radio 3 = 28.26)
            Console.WriteLine("AREA DEL CIRCULO");
            Console.Write("Digite el radio: ");
            radio = Convert.ToDouble(Console.ReadLine());
            areaCirculo = AreaCirculo(radio);
            Console.WriteLine("El area del circulo es: " + areaCirculo);
            Console.WriteLine();

            // edad (ejemplo: 20 = mayor de edad)
            Console.WriteLine("MAYORIA DE EDAD");
            Console.Write("Digite la edad: ");
            edad = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine(MensajeEdad(edad));
            Console.WriteLine();

            // resumen
            Console.WriteLine("========================================");
            Console.WriteLine("  RESUMEN DE LOS RESULTADOS");
            Console.WriteLine("========================================");
            Console.WriteLine("Area del triangulo: " + areaTriangulo);
            Console.WriteLine("Area del cuadrado: " + areaCuadrado);
            Console.WriteLine("Area del circulo: " + areaCirculo);
            Console.WriteLine(MensajeEdad(edad));
            Console.WriteLine();
            Console.WriteLine("Presione una tecla para salir...");
            Console.ReadKey();
        }
    }
}