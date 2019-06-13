# İçerik

Bu depo aylardır merak ettiğim Go dilini öğrenmek ve Web'in temel çalışma mekanizmasını daha iyi kavrayabilmek için oluşturulmuştur.Depoda temel programlama işlevleri (döngüler , koşullu ifadaler vs.) ile ilgili örnekler olacaktır ve belki ufak bir web projesi içerebilir. Umarım benim gibi Go dili öğrenmek isteyenler için faydalı olur.

# Kaynak

Bu depoyu hazırlarken faydalanacağım kaynaklar.
- [Go Examples](https://gowebexamples.com/)
- [Go Lang Docs](https://golang.org/doc/articles/wiki/)
- [Web Application with Go Lang](https://github.com/astaxie/build-web-application-with-golang/)

# Kurulum

Go hızlı derlenmiş, garbage-collected, eş zamanlı işlem yapabilen  sistem programlama dilidir.Bu özelliklerin getirdiği bazı avantajlar mevcuttur.

[Download](https://golang.org/dl/) adresine giderek gerekli adımları gerçekleştirin.

- Go geliştirme araçlarını ve bağımlıklarını kullanabilmek için bir workspace dizini oluşturmamız gerekiyor.Bu dizin gerekli kütüphane ve geliştirme dosyalarını içerecektir.
- Oluşturduğumuz dizine gidip "src" , "bin" ve "pkg" adında alt dizinler oluşturuyoruz
- Diğer adımları gerçekleştirmek için bu deopdan faydalanabilirsiniz [Kaynak](https://github.com/astaxie/build-web-application-with-golang/blob/master/tr/01.2.md)

- bin : Çalıştıralabilir dosyaları içerir
- pkg : Derlenmiş dosyaları içerir
- src : Kaynak dosyalarını içerir

# Go Komutları

Terminalde "go" komutunu çalıştırarak komutları görebilirsiniz

#Paketler

Paket ve kaynak dosyaları $GOPATH/src/<A>/B.go şeklinde oluşturun (A paketin ismidir) 

# go build

Go paketlerini derlemek için kullanılır , eğer paket main değilse go build çalıştığında hiçbir şey oluşturmayacaktır

Eğer paketinizin derlenmiş halini /pkg dizininde .a uzantılı derlenmiş halini istiyorsanız go install komutunu kullanmanız gerekmektedir

Eğer paket main ise aynı dizin içinde çalıştırılabilir hali oluşturulacaktır.Dosyanın /bin içinde olmasını istiyorsanız go install komutunu kullanmanız gerekmektedir
