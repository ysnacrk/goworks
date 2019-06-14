# Değişkenler

### Değişken tanımlama

Go dilinde tip değişken isminden sonra yazılır

```
var <değişken ismi> <değişken tipi>

```

Birden fazla değişken tanımlayabilirsiniz

```
var <değişken1> , <değişken2> <değişken tipi>

```

Öntanımlı değeri olan değişken tanımlama

```

var <değişken1> , <değişken2> = <değer1> , <değer2>

```

Öz ifade ile değişken tanımlama


```

<değişken> := <değer>

```

Öz ifade kullanarak `var` ve `type` anahtar kelimlerini kullanmak zorunda değiliz fakat öz ifadeyi sadece fonkisyonların içerisinde değişken tanımlarken kullanabiliyoruz global scope'ta değişken tanımlarken `var` anahtar kelimesini kullanmalıyız.


### Sabitler (Constants)

Sabitler derleme zamanında oluşturulan ve runtime'da değişmeyen değişkenlerdir.

```

const euler_value float32 =  2.7182818

```

### Sayı(Integer , float ...) Tipleri

Integer tipleri işaretli ve işaretsiz olmak üzere ikiye ayrılıyor. Go bunları `int` ve `uint` olarak tanımlar.Go ile `int8` ,  `int16` , `int32` , `int64` , `byte` gibi integer tipleri de tanımlamak mümkün.

`rune` , `int32` ' ye ve `byte` ,`uint8`'e karşılık gelir.


Go'da malesef tipler arası atama yapılamıyor

```
var x int8

var y int32

z := x + y

```

Yukarıdaki kod  `invalid operation: x + y (mismatched types int8 and int32)` hatası verecektir.

Float değişkenler için `float32` ve `float64` tipleri kullanılır.

```

var euler_value float32 =  2.7182818

```

Eğer tip belirtmezseniz default olarak `float64` tipinde oluşturulur

Go'da karmaşık sayı tanımlamakta mümkün `Gerçel + Sanal`

complex64(32 bit gerçel ,32 bit sanal kısım) ve complex128(64 bit gerçel , 64 bit sanal kısım) olarak ikiye ayrılır.

```

var x complex128 = 7 +8i

```

### Boolean

```

var isDone bool = true


```


### Strings

Stringler çift tırnak `""` veya ```` olarak gösterilebiliyor

```

var <değişken1> string = "abcd"
<değişken2> := "cdef"

```

Go'da indis değerleini değiştiremezsiniz fakat okuyabilirsiniz !

Stringin içindeki bir karakteri değiştirmek istiyosanız

```

a := "abcd"
b := []byte(a) //byte tipine çeviriyoruz
b[1] = 'c'
d := string(b) //string tipine çeviriyoruz

```

`+` operatörüyle iki stringi birleştirebilirsiniz


```

a := "abc"
b := "def"
c := a + b

```


