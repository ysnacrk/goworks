
# Kurulum

Go hızlı derlenmiş, garbage-collected ve eş zamanlı işlem yapabilen  sistem programlama dilidir.Bu özelliklerin getirdiği bazı avantajlar mevcuttur.

[Download](https://golang.org/dl/) adresine giderek gerekli adımları gerçekleştirin.

- Go geliştirme araçlarını ve bağımlılıklarını kullanabilmek için bir workspace dizini oluşturmamız gerekiyor.Bu dizin gerekli kütüphane ve geliştirme dosyalarını içerecektir.
- Oluşturduğumuz dizine gidip "src" , "bin" ve "pkg" adında alt dizinler oluşturuyoruz
- Diğer adımları gerçekleştirmek için bu deopdan faydalanabilirsiniz [Kaynak](https://github.com/astaxie/build-web-application-with-golang/blob/master/tr/01.2.md)

- bin : Çalıştıralabilir dosyaları içerir
- pkg : Derlenmiş dosyaları içerir
- src : Kaynak dosyalarını içerir

# Go Komutları

Terminalde "go" komutunu çalıştırarak komutları görebilirsiniz

# Paketler

Paket ve kaynak dosyaları <workspace>/src/<A>/B.go şeklinde oluşturulur (A paketin ismidir). Paket için src altında yeni bir dizin oluşturmalısınız.$GOPATH/src/A/B/C oluşturursanız , paket yolu A/B/C olacaktır. Paket ismi ise enson dizinin ismi olacaktır(C).

Paketleri kullanamabilmek için ilk önce derlememiz gerekiyor.Paketimizin bulunduğu dizine giderek 

``` 
go install 

```
komutunu çalıştırıyoruz



# go build

Go paketlerini derlemek için kullanılır , eğer paket main değilse go build çalıştığında hiçbir şey oluşturmayacaktır

Eğer paketinizin derlenmiş halini <workspace>/pkg dizininde .a uzantılı derlenmiş halini istiyorsanız go install komutunu kullanmanız gerekmektedir

Eğer paket main ise aynı dizin içinde çalıştırılabilir hali oluşturulacaktır.Dosyanın <workspace>/bin içinde olmasını istiyorsanız go install komutunu kullanmanız gerekmektedir

```
go build a.go

```
Argüman almaz ise dizindeki tüm dosyaları derleyecektir

# go fmt

Go dili söz dizimi kurallarına çok önem verir ve dikkat eder bu yüzden söz dizimi kurallarını yönetmek için böyle bir komut kullanılır

```
go fmt a.go

```

# go get 

Üçüncü parti paketleri projelerinize entegre etmenizi sağlar.

```
go get github.com/astaxie/beedb

```

# go install 

Bütün paketleri derleyip , <workspace>/bin dizini altına taşır

# go doc 

Go paketleri hakkında bilgi almanızı sağlar

```
go doc fmt Printf

```

# go env

Ortam değişkenlerini listeler

# go list

Yüklü olan paketleri listler

# go fix 

Versiyon güncelleme

# go version

Sürüm bilgisi

# go run 

Geçici olarak derleyip çalıştırma

# go help

Komutlar hakkında daha geniş bilgilere erişebilirsiniz

```
go help run

```