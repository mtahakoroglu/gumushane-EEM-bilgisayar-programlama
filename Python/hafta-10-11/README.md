<h3>LİSTELERLE ÇALIŞMA (WORKING with LISTS) - SON BİR ÖRNEK</h3>

<h4>SON BİR ÖRNEK</h4>
<p align="justify">Ara sınavdan hemen önceki son dersimizin son örneğinde Python listelerine ait <b>pop()</b> metodunu kullanarak listeden elemanları atmıştık. Fakat bunu sınavda sormamıştık. Burada <b>pop()</b> metodunu da kullanarak son bir örnek yaparak yavaştan <b>numpy</b> paketi kullanmaya geçeceğiz. Bu örnekte ayrıca Python'da <b>debug</b> modunda kodu istediğimiz satırlarda durdura durdura kodu çalıştırmayı göreceğiz. İngilizce'de böcek kelimesinin karşılığı <b>bug</b>. Dolayısıyla <b>debug</b> böceklerden temizlemek mânâsına geliyor. Buradaki analoji kodumuzu hatalardan temizlemek oluyor yâni. İlgili videoyu izlemek için tıklayınız.</p>

<b>list_methods_exercise.py</b>

```
names = ["Önder", "Safa", "Abdullah"]
print(f"names = {names}")
# listenin sonuna yeni bir isim ekleyelim
names.append("Çınay")
print(f"names = {names}")
# listenin sonuna bir isim daha ekleyelim
names.append("Cindy")
print(f"names = {names}")
# listenin başına yeni bir isim ekleyelim
names.insert(0, "Abdurrahman")
print(f"names = {names}")
# listenin başından ikinci sıraya yeni bir isim ekleyelim
names.insert(1, "Sefa")
print(f"names = {names}")
# listenin başından üçüncü sıradaki ismi silelim
names.pop(2)
print(f"names = {names}")
```

<h4>LİSTEDEN ÇIKARDIĞIMIZ ELEMANLARI AYRI BİR LİSTEDE TOPLAMAK</h4>

<p align="justify">Dersin ikinci kısmında <b>numpy</b> pkaeti kullanarak matrislerde elemanlara erişmeye bakacaktık. Ancak dersin içinde Sefa Dalma arkadaşımızın bir sorusu/önerisi üzerine elimizde bulunan bir isim listesinden baş harfi 's' ile başlayan isimleri çıkarıp bu isimleri ayrı bir listeye kaydetme probleminin kodunu yazmaya çalıştık. Derste for döngüsü kullanarak yapmaya çalıştığımızda hata vermişti. Aşağıda while döngüsü ile çözümü verilen problemin videosunu izlemek için tıklayınız.</p>

<b>popped_elements_new_list.py</b>

```
names = ["Ali", "berat", "Cindy", "davud", "SAFA",
         "Ece", "sefa", "Gizem", "Selin", "İsmail"]
print(f"names = {names}")
print(f"names isimli listede {len(names)} kişi vardır.")
# listeden baş harfi S ile başlayan isimleri listeden çıkaracağız
popped_names = []
i = 0
while i < len(names):
    if names[i][0].upper() == "S":
        popped_names.append(names.pop(i))
    else:
        i += 1
print(f"Çıkarılan isimler = {popped_names}")
print(f"İlk listenin son hâli = {names}")
```