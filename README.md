# Bozukluk Hesaplama

Bu proje, belirli bir tutarın minimum bozukluk sayısını hesaplayan bir Python programını içerir.

## Kod

Aşağıdaki Python kodu, bozuklukların minimum sayısını hesaplamak için kullanılır. Recursion kullanılmıştır.

```python


def min_bozukluk_adedi(tutar):
    bozukluklar=[]
    a=tutar
    while a>=0.50:
        a=a-0.50
        bozukluklar.append(0.50)
    while a>=0.25:
        a=a-0.25
        bozukluklar.append(0.25)
    while a>=0.10:
        a=a-0.10
        bozukluklar.append(0.10)
    while a>=0.05:
        a=a-0.05
        bozukluklar.append(0.05)
    while a>=0.01:
        a=a-0.01
        bozukluklar.append(0.01)
    return tutar,len(bozukluklar),bozukluklar

print(min_bozukluk_adedi(2.83))
