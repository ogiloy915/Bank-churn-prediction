
# Sirroz bemorlari omon qolish prognozini aniqlash

Ushbu loyiha sirroz (jigar kasalligi) bilan og‘rigan bemorlarning omon qolish ehtimolini sun’iy intellekt yordamida prognoz qilishga qaratilgan.

## Maqsad

Tibbiy ma’lumotlar asosida bemorlarning omon qolish statusini bashorat qilish, shuningdek klasslar orasidagi disbalans muammosini SMOTE orqali yechish.

## Ishlatilgan texnologiyalar

- Python
- Pandas, NumPy
- scikit-learn
- imbalanced-learn (SMOTE)
- Matplotlib, Seaborn

## Ma’lumotlar

Model `Status` ustuniga qarab klassifikatsiya qildi:
- 0: vafot etgan
- 1: ehtimol
- 2: omon qolgan

Klasslar soni nomutanosib bo‘lgani sababli SMOTE yordamida balanslashtirildi.

## Model

- Model: `RandomForestClassifier`
- SMOTE orqali balanslangan `X` va `y` dan foydalanilgan
- `train_test_split` yordamida model o‘qitilgan va test qilingan

## Natijalar

Model quyidagi ko‘rsatkichlarga erishdi:

**Aniqlik (Accuracy):** `91%`

**Classification Report:**
| Klass | Precision | Recall | F1-score |
|-------|-----------|--------|----------|
| 0     | 0.89      | 0.89   | 0.89     |
| 1     | 0.98      | 0.96   | 0.94     |
| 2     | 0.87      | 0.88   | 0.90     |

**Confusion Matrix:**
![Confusion Matrix](confusion_matrix.png)

## Xulosa

- SMOTE yordamida klasslar balanslashtirildi
- Random Forest modeli yuqori aniqlikka erishdi
- Loyihada amaliy tibbiy klassifikatsiya muammosi muvaffaqiyatli yechildi

## Muallif

Oʻgʻiloy — 2025-yil, AI asosida sog‘liqni saqlashda klassifikatsiya modeli
