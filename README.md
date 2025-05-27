# 🏨 Predicción de Cancelaciones de Reservas en Hoteles

Este proyecto utiliza Machine Learning para predecir la probabilidad de que una persona cancele su reserva en un hotel. El modelo ha sido entrenado usando **Scikit-learn** en **Google Colab**, aprovechando técnicas de clasificación y análisis exploratorio para entender los factores que más influyen en la cancelación.

---

## 🔍 Objetivo

Anticiparse a las cancelaciones de reserva en hoteles para:
- Optimizar la gestión de habitaciones.
- Ajustar campañas de marketing y promociones.
- Minimizar pérdidas por cancelaciones inesperadas.

---

## 🧠 Tecnologías Usadas

- Python 3
- Scikit-learn
- Pandas, NumPy, Matplotlib, Seaborn
- Google Colab
- Jupyter Notebook

---

## 📂 Estructura del Proyecto
```
📁 hotel-cancellation-prediction/
├── data/
│ └── hotel_bookings.csv
├── modelo_final.pkl
├── Hotel_Cancellation_Model.ipynb
└── README.md
```

---

## 📊 Dataset

Se utiliza el dataset público de reservas de hoteles:  
**[Hotel Booking Demand Dataset](https://www.sciencedirect.com/science/article/pii/S2352340918315191)**  
Contiene información como:
- Tipo de hotel
- País de procedencia
- Número de adultos/niños
- Fechas de llegada/salida
- Solicitudes especiales
- Si la reserva fue cancelada (`is_canceled`)

---

## 🔧 Entrenamiento del Modelo

### 1. Preprocesamiento
- Limpieza de datos nulos
- Codificación de variables categóricas (One-Hot Encoding)
- Escalado de variables numéricas

### 2. Selección del Modelo
- Modelos evaluados: Random Forest, Logistic Regression, Gradient Boosting
- Métricas: Accuracy, Precision, Recall, F1-score, ROC AUC

### 3. Modelo Final
- **Random Forest Classifier** fue seleccionado como el modelo más robusto.
- Accuracy: 87%
- ROC AUC: 0.91

---

## 💾 Cómo usar el modelo

1. Abre el notebook en [Google Colab](https://colab.research.google.com).
2. Sube el archivo `hotel_bookings.csv` a la carpeta `/content`.
3. Ejecuta cada celda para entrenar y usar el modelo.
4. El modelo puede exportarse como `.pkl` para su uso en producción.

---

## ▶️ Ejemplo de uso

``` python
import joblib
modelo = joblib.load('modelo_final.pkl')
nueva_reserva = [[0, 2, 0, 0, 1, 3, 0, 0, 1, 0]]  # ejemplo ficticio
modelo.predict_proba(nueva_reserva)
```
## 📈 Próximos pasos
Implementar el modelo en una API web.

Crear dashboard con Power BI o Streamlit para visualizar predicciones en tiempo real.

Ajustar hiperparámetros con GridSearchCV.

## 🤝 Contribuciones
¡Se aceptan contribuciones! Puedes hacer un fork del proyecto, trabajar en una rama y enviar un Pull Request.

## 📬 Contacto
Desarrollado por Ángel Troncoso  
📧 Email: angeltroncoso2019@outlook.es  
🔗 LinkedIn[www.linkedin.com/in/angeltroncoso]  
🚀 GitHub [https://github.com/AngelTroncoso]  

##⚠️ Licencia
Este proyecto está licenciado bajo MIT License.



