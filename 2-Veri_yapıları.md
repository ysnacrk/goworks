# Veri Yapıları


## Çoklu Değişken Tanımlama

```
cont (
    a = "Deneme"
    b = "Merhaba"
    c = "Go"
)

var (

    x = 0
    y = 18
    z = 78

)

```

Şeklinde çoklu değişken tanımlayabiliyoruz.


## Iota

`iota` anahtar kelimesi artan bir şekilde değişkenleri numaralandırmak için kullanılır

```

const (
    a = iota // 0
    b = iota // 1
    c = iota // 2
    
)

const (
    a , b , c = iota , iota , iota // hepsi 0 değerini alacaktır çünkü iota yeni satıra geçtiği zaman değeri artar
)
 

```


## Array

Bir `array` tanımlamak için `var dizi_ismi[BOYUT]değişken_tipi` söz dizimi kullanımalıdır.


```
    var a[2]string
    a[0] = "merhaba"
    a[1] = "go"
    fmt.Println(a[0], a[1])

```

Şeklinde basit bir string dizisi tanımlayabilirsiniz.


Daha kısa bir şekilde dizi tanımlamak istiyosanız 

```
    primes := [6]int{2, 3 ,5 ,7 11 ,13}
```

ifadesi kullanılabilir


## Slices

Diziler sabit bir uzunluğa sahiptir fakat `Slices` dinamik bir yapıya sahiptir

Bir `slice` tanımlamak için ` var slice_ismi[]değişken_tipi` şeklinde tanımlanabilir.Array tanımlaya benziyor sadece boyut bilgisini belirtmiyoruz.

```

    primes := [6]int{2, 3 ,5 ,7 11 ,13}
    var s []int = primes[1:4]
```

Slicelar veri kaydetmez sadece dizinin bir kısmını tanımlar.Eğer iki slice ortak bir kısmız paylaşıyor ise birinde yapılan bir değişiklik diğerinindekini de etkileyecektir

```

isimler := [4]string{
    
    "Ali",
    "Veli",
    "Mehmet",
    "Ahmet",
}


fmt.Println(isimler)

a := names[0:2]
b := names[1:3]

fmt.Println(a,b)

b[0] = "AAA"
fmt.Println(a ,b)
fmt.Println(isimler)

```


```
Output : 

[Ali Veli Mehmet Ahmet]
[Ali Veli] [Veli Mehmet]
[Ali AAA] [AAA Mehmet]
[Ali AAA Mehmet Ahmet]

```