---
title: Regresi Logistik Biner
tags: [analisis data kategori]
style: fill
color: warning
description : Catatan mahasiswa ibu yang luhur
---

{% capture list_items %}
Metode Regresi
Regresi Logistik Biner
{% endcapture %}
{% include elements/list.html title="Table of Contents" type="toc" %}

### Metode Regresi

> Metode regresi merupakan analisis data yang mendeskripsikan hubungan kualitas antara variabel respon dan prediktor (Hosmer dan Lemeshow, 2000)

Apa perbedaan mendasar antara regresi linier dan regresi logistik?
* Perbedaan mendasarnya adalah dari tipe data variabel responnya
* Regresi logistik merupakan salah satu metode yang dapat digunakan untuk mendapatkan hubungan antara variabel respon yang bersifat **kategorik** dengan variabel prediktor (Agresti, 1990)

Apa itu regresi logistik biner?
* Regresi logistik biner adalah regresi dengan variabel respon yang mempunyai 2 kategori atau 2 kejadian
* Jenis data pada variabel prediktor dapat berupa nominal, ordinal, interval, maupun rasio

### Regresi Logistik Biner

> Regresi logistik merupakan suatu metode analisis data yang digunakan untuk mencari hubungan antara variabel respon (y) yang bersifat **biner** atau dikotomus dengan variabel prediktor (x) yang bersifat polikotomus (Hosmer dan Lemeshow, 1989)

Outcome dari variabel respon y terdiri dari 2 kategori yaitu "sukses" dan "gagal" yang dinotasikan dengan y=1 (sukses) dan y=0 (gagal).

Variabel y mengikuti distribusi **Bernoulli** untuk setiap observasi tunggal.

Fungsi probabilitasnya adalah:
![image](https://user-images.githubusercontent.com/71642722/121794635-38e79980-cc34-11eb-8f5c-64800dca647e.png)

Dimana jika y = 0, maka f(y) = 1 - π, dan jika y = 1, maka F(y) = π.

Fungsi regresi logistik dapat dituliskan sebagai berikut:
![image](https://user-images.githubusercontent.com/71642722/121794696-ae536a00-cc34-11eb-888c-b648fc787bea.png)

dengan,
![image](https://user-images.githubusercontent.com/71642722/121794706-bd3a1c80-cc34-11eb-9813-b27dca120618.png)

Nilai z antara -∞ dan +∞ sehingga nilai f(z) terletak antara 0 dan 1 untuk setiap nilai z yang diberikan.

Hal tersebut menunjukkan bahwa **model logistik menggambarkan probabilitas atau resiko dari suatu objek**

Model regresi logistiknya adalah sebagai berikut:
![image](https://user-images.githubusercontent.com/71642722/121794741-10ac6a80-cc35-11eb-8b16-ea1ff654e21b.png)

dimana p = banyaknya variabel prediktor.

Untuk mempermudah pendugaan parameter regresi, maka model regresi logistik pada persamaan diatas diuraikan dengan menggunakan transformasi logit dari π(x).

![image](https://user-images.githubusercontent.com/71642722/121803511-3e60d600-cc6c-11eb-86ad-cd16900adc73.png)

Sehingga diperoleh persamaan berikut 

![image](https://user-images.githubusercontent.com/71642722/121803533-533d6980-cc6c-11eb-9300-fc172d57a03c.png)

**Model tersebut merupakan fungsi linier dari parameter-parameternya.**

Dalam model regresi linier, diasumsikan bahwa amatan dari variabel respon diekspresikan sebagai y = E(Y|x) + ε, dimana

![image](https://user-images.githubusercontent.com/71642722/121803591-98fa3200-cc6c-11eb-8389-0065ed403dbc.png)

merupakan rataan dari populasi dan **ε diasumsikan mengikuti sebaran normal dengan rataan nol dan varians konstan.**

#### Estimasi Parameter

> Estimasi parameter dalam regresi logistik dilakukan dengan metode **Maximum Likelihood.**

Metode tersebut **mengestimasi parameter β dengan cara memaksimumkan fungsi likelihood** dan **mensyaratkan bahwa data harus mengikuti suatu distribusi tertentu.**

**Pada regresi logistik, setiap pengamatan mengikuti distribusi bernoulli** sehingga dapat ditentukan fungsi likelihoodnya.

Jika xi dan yi adalah pasangan variabel bebas dan terikat pada pengamatan ke-i, dan diasumsikan bahwa setiap pasangan pengamatan saling independen dengan pasangan pengamatan yang lainnya, i = 1, 2, ..., n.

Maka **fungsi probabilitas untuk setiap pasangan** adalah sebagai berikut:

![image](https://user-images.githubusercontent.com/71642722/121803829-803e4c00-cc6d-11eb-87d3-a98c0acda9c4.png)

dengan,

![image](https://user-images.githubusercontent.com/71642722/121803837-8a604a80-cc6d-11eb-8a73-abb6ffaed048.png)

dimana ketika j = 0, maka nilai xij = xi0 = 1.

**Setiap pasangan pengamatan diasumsikan independen**, sehingga fungsi likelihoodnya merupakan gabungan dari fungsi distribusi masing-masing pasangan, yaitu sebagai berikut:

![image](https://user-images.githubusercontent.com/71642722/121803869-aa900980-cc6d-11eb-85ea-16e5474c02a8.png)

Fungsi likelihood tersebut lebih mudah dimaksimumkan dalam bentuk log l(β) dan dinyatakan dengan L(β).

![image](https://user-images.githubusercontent.com/71642722/121803924-dad7a800-cc6d-11eb-8a16-59f81ad12d1f.png)

Nilai β maksimum didapatkan melalui turunan L(β) terhadap β. Dan hasilnya adalah sama dengan nol.

