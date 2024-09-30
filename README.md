Bu kod Rüya'nın manvında seçilen meyvenin fiyatını getiriyor. Switch case ile yazıldı.


'''


using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace switch_case_pratik1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            
            //Bu kod Rüya'nın manvında seçilen meyvenin fiyatını getiriyor. Switch case ile yazıldı.

            Console.WriteLine("Rüya'nın Manavına Hoş Geldiniz!");
            Console.WriteLine("Elma: 2 TL \nArmut: 3 TL \nÇilek: 4 TL \nMuz: 5 TL\nDiğer Bütün Meyveler: 6 Tl.");
            Console.WriteLine();
            Basla: //Tek bir sorgudan sonra bitmemesi için goto ifadesini kullandım, goto Başla diyerek buraya tekrar dönmesini sağladım.
            Console.WriteLine("Hangi meyveyi seçmek istersiniz? (Elma, Armut, Çilek, Muz, Diğer)");


            string meyve = Console.ReadLine().ToLower(); // Farklı şekilde yazıldığında caselerin dışına çıkmasın diye toLower ifadesini kullanarak girilen ifadenin küçük harfe dönüşmesini sağladım.
            switch (meyve)
            {
                case "elma":
                    Console.WriteLine("Seçtğiniz meyvenin fiyatı: 2 TL");
                    Console.WriteLine();// goto ile başa döndüğünde üstteki mesaj ile arada boşluk olsun diye eklendi, diğer case ler için de geçerli.
                    break;
                case "armut":
                    Console.WriteLine("Seçtğiniz meyvenin fiyatı: 3 TL");
                    Console.WriteLine();
                    break;
                case "çilek":
                    Console.WriteLine("Seçtğiniz meyvenin fiyatı: 4 TL");
                    Console.WriteLine();
                    break;
                case "muz":
                    Console.WriteLine("Seçtğiniz meyvenin fiyatı: 5 TL");
                    Console.WriteLine();
                    break;
                default: 
                    Console.WriteLine("Seçtiğiniz meyvenin fiyatı: 6 TL'dir.");
                    Console.WriteLine();
                    break;

            } 

            goto Basla;

            Console.Read();
        }
    }
}

