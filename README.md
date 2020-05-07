## Döngü içinde değişken nasıl tanımlarım?

Benzer şekilde yaratılan değerlerim var. Bunları bir döngü içinde değişik isimli değişkenlere atamak istiyorum. Örneğin:

```
for i in [1, 2, 3, 4, 5]:
	kare_i = i * i
```

gibi bir kod ile `kare_1` `kare_2` gibi değişkenler elde etmek istiyorum. Nasıl yaparım?

### Cevap:

Güçlükle, ve yapılması hiç tavsiye edilmeyen yöntemlerle. Farklı değişkenler yerine, değerlerin hepsini tutan tek bir liste kullanmalısın:

```
kareler = [] # boş liste
for i in [1, 2, 3, 4, 5]:
	kareler.append(i * i) # listeye kare ekle

# kare_1 yerine
print(kareler[0]) # 1

# kare_2 yerine
print(kareler[1]) # 4
```

Listeleri kullanmaya alıştıkça <strike>hayatının</strike> bir sürü şeyin kolaylaştığını görebilirsin:

```
kareler = [i*i for i in [1, 2, 3, 4, 5]]
```

Eğer 0, 1... yerine kendi indislerini kullanmak istiyorsan [sözlüklere][dict] veya [fonksiyonlara][function] bir göz atman lazım.

[dict]: https://python-istihza.yazbel.com/sozlukler.html
[function]: https://python-istihza.yazbel.com/fonksiyonlar.html
