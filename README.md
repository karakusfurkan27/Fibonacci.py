### Fibonacci Deseni Python Uygulaması

Bu Python programı, Fibonacci dizisinin bir desenini oluşturur. Fibonacci dizisi, her bir terimin kendisinden önceki iki terimin toplamına eşit olduğu bir sayı dizisidir. Bu program, Fibonacci dizisini kullanarak her bir adımda yıldız (`*`) işareti ile bir desen oluşturur.

#### Özellikler:
- Program, belirli bir sayıya kadar Fibonacci dizisinin terimlerini hesaplar.
- Her bir Fibonacci terimi ile ilişkili olarak, trigonometrik fonksiyonlar (kosinüs ve sinüs) kullanılarak yatay konumlandırma yapılır.
- Desende, her Fibonacci terimi için bir yıldız işareti yerleştirilir ve bu yıldızlar belirli bir mesafeye yerleştirilir.
- Desen, sayı arttıkça büyüyen bir şekilde görüntülenir.

#### Kullanım:
Program, `fibonacci_pattern(n)` fonksiyonu ile çalışır. Bu fonksiyon, `n` kadar Fibonacci terimi üreterek her birini desen şeklinde ekrana yazdırır.

#### Kurulum ve Çalıştırma:
1. Python yüklü olduğundan emin olun.
2. Aşağıdaki gibi bir Python dosyası oluşturun:
   ```python
   import math

   def fibonacci_pattern(n):
       a, b = 0, 1
       for i in range(n):
           x, y = int(math.cos(i) * b), int(math.sin(i) * b)
           print(" " * (x + 20) + "*")
           a, b = b, a + b
   ```

3. Programı çalıştırmak için `fibonacci_pattern(20)` gibi bir çağrı yapabilirsiniz. Buradaki `20` değeri, Fibonacci dizisinin ilk 20 terimi için deseni oluşturur.

#### Parametreler:
- `n`: Fibonacci dizisinin terim sayısı. Bu parametre, ekrana basılacak yıldızların sayısını belirler.

#### Çıktı:
Program, Fibonacci dizisinin her terimi için aşağıdaki gibi bir desen oluşturur. Her bir terim, bir yıldız (`*`) işaretiyle ekrana basılır ve bu işaretlerin yatayda belirli bir mesafede yer almasını sağlamak için trigonometrik hesaplamalar yapılır.

#### Örnek Çıktı:
```
                     *
                    *
                      *
                       *
                      *
                       *
```

#### Notlar:
- Yıldızların yerleştirildiği mesafe, Fibonacci dizisindeki terimlerin büyüklüğüne göre değişir.
- Bu desen, Fibonacci dizisini daha estetik bir biçimde görselleştirir.
