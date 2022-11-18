# pop
using System;

namespace ConsoleApp2
{




    class Automobile
    {
        string marka;
        protected string color;
        public int weight;
        protected internal int max_speed;
        internal int height;
        public void dannye(int max_speed, int weight, int height)
        {
            Console.WriteLine("Автомобиль весом " + weight + " кг " + " высотой " + height + " см " + " может развивать максимальную скорость " + max_speed + " км/ч");
            Console.Read();
        }
    }
   
    class Program
    {
        static void Main(string[] args)
        {

          

            void SayHello()
            {
                Console.WriteLine("Привет! вот мой некоторые данные" );
                string name = "Алексей";
                int age = 18;
                double height = 187;
                Console.Write($"Имя: {name}  Возраст: {age}  Рост: {height}м");
                Console.WriteLine("Щас будет преставлен калькулятор, введите первое число и ннажмите ");
               
            }
            void Pop()
            {
                double a;
                double b;
                double c;
                char h;

                Console.WriteLine("Введите первое число:");
                a = Convert.ToDouble(Console.ReadLine());

                Console.WriteLine("Введите +,-,*,/");
                h = Convert.ToChar(Console.ReadLine());

                Console.WriteLine("Введите второе число:");
                b = Convert.ToDouble(Console.ReadLine());

                if (h == '+')
                {
                    c = a + b;
                    Console.WriteLine("Cумма " + a + " и " + b + " равна " + c + ".");
                }

                else if (h == '-')
                {
                    c = a - b;
                    Console.WriteLine("Разность " + a + " и " + b + " равна " + c + ".");
                }

                else if (h == '*')
                {
                    c = a * b;
                    Console.WriteLine("Умножение " + a + " на " + b + " равно " + c + ".");
                }

                else if (h == '/')
                {
                    c = a / b;
                    Console.WriteLine("Деление " + a + " на " + b + " равно " + c + ".");
                }
                else
                {
                    Console.WriteLine("Неизвестный оператор.");
                   
                }
             

                Automobile VAZ = new Automobile();
                Console.WriteLine("Введите максимальную скорость автомобиля км/ч");
                VAZ.max_speed = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Введите вес автомобиля в кг");
                VAZ.weight = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Введите высоту автомобиля в см");
                VAZ.height = Convert.ToInt32(Console.ReadLine());
                VAZ.dannye(VAZ.max_speed, VAZ.weight, VAZ.height);
            }
            SayHello();
            Pop();


        }

    }
}
