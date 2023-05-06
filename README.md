# calculator-in-cSharp
calculator in c#
using System;

namespace HesapMakinesi
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hesap Makinesi");
            Console.WriteLine("------------------");

            while (true)
            {
                Console.Write("Birinci sayıyı girin: ");
                double sayi1 = Convert.ToDouble(Console.ReadLine());

                Console.Write("İkinci sayıyı girin: ");
                double sayi2 = Convert.ToDouble(Console.ReadLine());

                Console.WriteLine("İşlem Seçin: ");
                Console.WriteLine("1 - Toplama");
                Console.WriteLine("2 - Çıkarma");
                Console.WriteLine("3 - Çarpma");
                Console.WriteLine("4 - Bölme");
                Console.WriteLine("0 - Çıkış");

                Console.Write("Seçiminizi yapın: ");
                int secim = Convert.ToInt32(Console.ReadLine());

                double sonuc = 0;

                if (secim == 1)
                {
                    sonuc = sayi1 + sayi2;
                    Console.WriteLine("Sonuç: " + sonuc);
                }
                else if (secim == 2)
                {
                    sonuc = sayi1 - sayi2;
                    Console.WriteLine("Sonuç: " + sonuc);
                }
                else if (secim == 3)
                {
                    sonuc = sayi1 * sayi2;
                    Console.WriteLine("Sonuç: " + sonuc);
                }
                else if (secim == 4)
                {
                    if (sayi2 != 0)
                    {
                        sonuc = sayi1 / sayi2;
                        Console.WriteLine("Sonuç: " + sonuc);
                    }
                    else
                    {
                        Console.WriteLine("Hata! Bölme işleminde ikinci sayı sıfır olamaz.");
                    }
                }
                else if (secim == 0)
                {
                    Console.WriteLine("Çıkış yapılıyor...");
                    break;
                }
                else
                {
                    Console.WriteLine("Hatalı seçim! Lütfen geçerli bir seçenek girin.");
                }

                Console.WriteLine("------------------");
            }

            Console.ReadLine();
        }
    }
}
