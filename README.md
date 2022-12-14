# GaussElimination
Patika.dev temel matematik dersi projesi olarak gauss eliminasyonu ile ilgili blog yazısı

# Gauss eliminasyonu
Gauss eliminasyonu, lineer denklem sistemlerinin çözmek için kullanılır. Peki bütün lineer denklem sistemlerini çözebilir mi? Matemetikte her metod ya da uygulama sihirli bir formülasyon olmadığından tek bir yöntem tüm sorunlara çare olmadığı gibi Gauss Eliminasyonu da bütün lineer denklem sistemleri için kullanılamaz. O zaman biz hangi lineer denklem sisteminde Gauss eleminasyonunu kullanmamız gerektiğini nasıl anlayacağız? Cevabı çok basit. Bilinmeyen sayısı ile denklem sayımızın aynı olduğu sistemlerde Gauss eliminasyonunu çok rahat, çok profesyonel bir şekilde kullanabilir. Bunu daha da açarsak şu şekilde bir örnek ile açıklayalım:

* 2x+8y+2z=14   ___|

* x+6y-1z=13  ___| --------->        3 bilinmeyen(x,y ve z) ve bunlara bağlı 3 denklem var bu durumda Gauss eliminasyonunu kullanabiliriz
                    
* 2x-1y+2z=5 ___|


Denklemlerimiz ve bilinmeyen sayımız eşit ise sonraki adım olarak denklem sistemlerini genişletilmiş katsayılar matrisi biçimde yazmamız gerekli. Bu ne demek? Yukarıda görmüş olduğunuz denklem sistemine dikkatli bakarsanız aslında bir matris diziliminde olduğunu görebilirsiniz. Matrisi oluştururken önce her bilinmeyenin başındaki katsayıları alalım aynı sıra ile


| 2  8 2|

| 1 6 -1|  -------- bunu 3*3'lük bir matris olarak düşünün her katsayıyı yerleştirdik. bu matrisimize katsayılar matrisi diyoruz

|2  -1  2|



| 2  8 2|  |x|

| 1 6 -1|  |y|   ----------- ardından sütun halinde bilinmeyenlerimizi yine sıra ile ekledik. bu matrise ise bilinmeyen matrisi ismini veriyoruz

|2  -1  2|  |z|


| 2  8 2|  |x|____|14|

| 1 6 -1|  |y| = |13|  ----------- son adım olarak ise denklemlerimiz sonuçlarını yine sıra ile sütun halinde ekledik. son matrisimiz ise değerler matrisidir.

|2  -1  2|  |z|_____|5|

Matrisimizi bu şekilde oluşturduk. bilmemiz gereken bir şey daha var. Matrislerde üst üçgen matris nedir öncelikle bunu bilmemiz lazım. Üst üçgen matrisinde, katsayılar matrisinin sol üst köşesinden sağ alt köşesine hayali bir köşegen çizersek köşegenin altında kalan elemanları 0'a eşitlediğimiz zaman üst üçgen matrisi oluşturmuş oluyoruz. İşte bu adımımızda katsayılar matrisini üst üçgen matrisi yapmamız gerekiyor. Bunu nasıl yapacağız? Katsayılar matrisimizizdeki köşegenimiz 3, -4 ve 8 elemanarından geçen köşegendir yani elde etmek istediğimiz üst üçgen matrisi şu şekilde görünmesi gerekir:

| 2  8 2|

| 0 6 -1|  

|0  0  2|

Bu hale getirmemiz için yapmamız gereken işlem ise şöyledir:
Bunu yapabilmek için ilk satır kullanılır. Yani alttaki 2 satırın ilk elemanlarını 0 yapmak için 1. satır ile toplandığında 0 olacak şekilde dönüştüreceğiz. şu şekilde anlatayım.
ilk satırımızın her bir elemanını -1/2 ile çarpıp 2. satır ile toplarsak, (-1/2)*2 + (-1)= 0 olur. 2. satırın ilk elemanı 0 olur ve 2. satırımız değişir. aynı şekilde 3. satırın ilk elemanını sıfır yapmak için ise 2*(-1) + 2 = 0 olur ve matrisimiz şu şekilde değişir.

| 2  8 2||x|____|14|

| 0 2 -2| |y| = |6|

|0  -9  0||z|_____|-9|

şimdi 3. satırın 2. elemanını da 0 yapmamız gerekli bunun için yine 2. satırımızla son satırımızın her bir elemanını topladığımızda 3. satırın 2. elemanını 0 yapacak şekilde düzenlememiz gerekli. Bunu da 2. satırımızı 9/2 ile çarpıp 3. satır ile toplamamız gerekecek. (2*9/2) + -9 = 0 olacak yeni matrisimiz ise şu şekli alacak:

| 2  8 2||x|____|14|

| 0 2 -2| |y| = |6|

|0  0  -9||z|_____|18|


şidmi istediğimiz noktaya geldik işte. Yapmamız gereken bir adım daha var. Alttan üste doğru bilinmeyenleri bulup yerine koyup diğer bilinmeyenleri bulacağız. 3. satırımıza baktığımızda sadece -9 kaldı ve bu z bilinmeyenimizi bulmamıza yardımcı olacak. şu şekilde -9z=18 ise z = -2. Şimdi z bilinmeyenimizi artık biliyoruz bu sayede diğer bilinmeyenleri bulmak daha kolay olacak. ikinci satırımıza bakalım burda da ufak bir denklem var: 2y-2z=6 burada z yi biliyoruz z=-2 bunu yerine koyduğumuz zaman 

2y-2*(-2)=6    

y=1

evet şimdi 3 bilinmeyenin ikisini biliyoruz artık son bilinmeyeni bulmak daha kolay. ilk satırımıza bakalım yine bir denklem var elimizde: 

2x+2y+2z=14 bulduğumuz y ve z bilinmeyenini yerine koyalım ve x'i bulalım

2x+2*(1)+2*(-2)=14

x=5

İşte! Gauss eleminasyon yöntemi bu kadar. Biraz karmaşık gelebilir fakat diğer kaynaklardan araştırırsanız daha iyi oturabilir. Okuduğunuz için teşekkürler





