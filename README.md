# Telco Customer Churn Dataset Müşteri Terk Oranı Görselleştirme

Bu Python script'i, Kaggle'daki Telco Customer Churn Dataset veri seti üzerinde müşteri terk oranını görselleştirmek için kullanılır.

## Kod Açıklaması

```python
import pandas as pd
import matplotlib.pyplot as plt

# Veri setini yükleme
data = pd.read_csv("C:/Users/caner/OneDrive/Documents/GitHub/TelcoCustomerChurn/WA_Fn-UseC_-Telco-Customer-Churn.csv")

# Müşteri terk oranını hesaplama
churn_counts = data['Churn'].value_counts()

# Müşteri terk oranını görselleştirme
plt.figure(figsize=(6, 6))
plt.pie(churn_counts, labels=churn_counts.index, autopct='%1.1f%%', colors=['skyblue', 'lightcoral'])
plt.title('Müşteri Terk Oranı')
plt.legend(['Müşteri Devam Ediyor', 'Müşteri Ayrılıyor'], loc='best')
plt.show()
```

## Örnek Kullanım

```bash
python churn_analysis.py
```

## Notlar

- Bu script, veri setindeki "Churn" sütununu kullanarak müşteri terk oranını görselleştirir.
- Mavi renk, müşterilerin devam ettiğini; kırmızı renk, müşterilerin ayrıldığını temsil eder.
- Veri seti ve görselleştirme için Matplotlib ve Pandas kütüphaneleri kullanılmıştır.

## Lisans

Bu script MIT lisansı altında dağıtılmaktadır. Detaylı lisans bilgileri için `LICENSE` dosyasına başvurun.
