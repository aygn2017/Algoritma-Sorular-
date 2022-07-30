   // * Kullanıcıdan pozitif bir sayı girmesini istiyoruz (n).
            // * Sonrasında ise kullanıcıdan n sayısı kadar pozitif sayı girmesini istiyoruz.
            // * Girilen bu sayıların içinden çift olanları ekrana yazdırıyoruz.

            Console.Write("Lütfen Pozitif Bir Sayı Giriniz :");
            int number = int.Parse(Console.ReadLine());
            if (number > 0)
            {
                int[] array = new int[number];
                for (int i = 0; i < number; i++)
                {
                    Console.Write("Bir Sayı Giriniz :");
                    int sayi = int.Parse(Console.ReadLine());   
                    array[i] = sayi;
                }
                for (int j = 0; j < number ; j++)
                {
                    if (array[j] % 2 == 0)
                    {
                        Console.WriteLine("Çift Sayılar :" + array[j]);
                    }
                    
                      // * Kullanıcıdan 2 adet pozitif sayı girilmesini istiyoruz (m,n)
            // * Kullanıcının girdiği n sayısı kadar tekrar sayı girilmesini istiyoruz.
            // * Bu girilen sayılardan hangileri m sayısına eşit veya tam bölünüyorsa ekrana yazdırıyoruz.

            Console.Write("Lütfen Bir Sayı Giriniz :");
            int ilkSayi = int.Parse(Console.ReadLine());

            Console.Write("Lütfen İkinci Sayıyı Giriniz :");
            int sonSayi = int.Parse(Console.ReadLine());

            int[] array = new int[ilkSayi];

            if (ilkSayi > 0 || sonSayi>0)
            {

            for (int i = 0; i < array.Length ; i++)
            {
                    Console.Write("Sayı Giriniz :" , i+1);
                    int sayi = int.Parse(Console.ReadLine());
                    array[i] = sayi;
            }

            for (int i = 0; i < array.Length; i++)
            {
                    if (array[i] == sonSayi)
                    {
                        Console.WriteLine(array[i] + ". Sayısı Girilen Son Sayıya Eşitttr.");
                    }
                    else if (array[i] % sonSayi == 0)
                    {
                        Console.WriteLine(array[i] + "Sayısı Girilen Son Sayıya Tam Bölünebilir.");
                    }
                    
                    
                    
                      // *Kullanıcıdan pozitif bir sayı girmesini istiyoruz (n).
            // *Sonrasında kullanıcıdan n sayısı kadar kelime girmesini istiyoruz.
            // *Girilen kelimeleri ekrana sondan başa yazdırıyoruz.

            Console.Write("Bir Sayı Giriniz : ");
            int number = int.Parse(Console.ReadLine());
            string[] words = new string[number];

            if (number > 0)
            {
                for (int i = 0; i < words.Length; i++)
                {
                    
                    Console.WriteLine("Kelime Giriniz.", i+1);
                    words[i] = Console.ReadLine();
                }

                for (int i = 0; i < words.Length; i++)
                {
                    char[] dizi= words[i].ToCharArray();
                    Array.Reverse(dizi);
                    string returnmetin = new string(dizi);
                    Console.WriteLine(returnmetin);
                }

                Array.Reverse(words);

                foreach (var item in words)
                {
                    Console.WriteLine(item);
                }
            }
            else
            {
                Console.WriteLine("LÜTFEN POZİTİF BİR SAYI GİRİNİZ!");
            }
