# Unsupervised Learning: Clustering

Ulgurji savdo mijozlarini xarajat turlariga qarab segmentlash loyihasi (K-Means klasterlash).

## Ma'lumotlar

[Wholesale Customers Data](https://archive.ics.uci.edu/ml/datasets/wholesale+customers) (UCI): 440 ta mijozning yillik xarajatlari. Kategoriyalar: `Fresh`, `Milk`, `Grocery`, `Frozen`, `Detergents_Paper`, `Delicassen`. Notebook ma'lumotni to'g'ridan-to'g'ri internetdan yuklaydi.

## Jarayon

1. **Tayyorlash:** `Channel` va `Region` ustunlari olib tashlandi, faqat xarajat ustunlari qoldi.
2. **Normallashtirish:** `StandardScaler`.
3. **Klasterlash:** `KMeans(n_clusters=3)`.
4. **Vizualizatsiya:** pairplot, `Fresh` va `Grocery` scatter plot, klasterlar bo'yicha o'rtacha xarajatlar bar grafigi.

## Natija: klasterlar bo'yicha o'rtacha xarajat

| Klaster | Fresh | Milk | Grocery | Frozen | Detergents_Paper | Delicassen |
|---|---|---|---|---|---|---|
| 0 | 8 936 | 4 229 | 5 848 | 2 167 | 1 914 | 1 102 |
| 1 | 34 540 | 5 860 | 6 123 | 9 842 | 981 | 3 664 |
| 2 | 8 705 | 20 534 | 30 466 | 1 933 | 14 759 | 2 459 |

- **Klaster 0:** barcha kategoriyalarda o'rtacha va past xarajatli mijozlar.
- **Klaster 1:** yangi (`Fresh`) va muzlatilgan (`Frozen`) mahsulotlarga ko'p sarflaydigan mijozlar. Bular mehmonxona, restoran va kafelarga o'xshaydi.
- **Klaster 2:** sut, oziq-ovqat va yuvish vositalariga ko'p sarflaydigan mijozlar. Bular chakana savdo do'konlariga o'xshaydi.

## Ishga tushirish

```bash
pip install -r requirements.txt
jupyter notebook unsupervised_learning_clustering.ipynb
```
