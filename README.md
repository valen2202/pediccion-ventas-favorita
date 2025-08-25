#  Store Sales Time Series Forecasting

Este proyecto nace como desafío inspirado en el **Kaggle Competition: Store Sales - Time Series Forecasting**.  
El objetivo: **predecir las ventas de una cadena de supermercados en Ecuador**, combinando factores como calendario, feriados, precio del petróleo y estacionalidad de las series temporales.

##  Motivación
Las ventas de retail no solo dependen de la demanda natural, sino también de variables externas (feriados, promociones, eventos globales).  
Este proyecto busca capturar esos patrones y construir un modelo robusto que pueda anticipar las ventas con mayor precisión.

##  Etapas del Proyecto
1. **Carga y preparación de datos**  
   - Conversión de fechas a `datetime`.  
   - Integración de datasets: feriados, petróleo y ventas.  

2. **Feature Engineering**  
   - Creación de variables de calendario (día, mes, año, día de la semana).  
   - Incorporación de feriados con variables dummy.  
   - Medias móviles sobre el precio del petróleo para capturar tendencias.  

3. **Exploratory Data Analysis (EDA)**  
   - Visualización de ventas vs precio del petróleo.  
   - Análisis de estacionalidad y tendencias.  

4. **Modelado**  
   - **XGBoost** y **LightGBM** como modelos principales.  
   - One-hot encoding en variables categóricas (`family`).  

5. **Evaluación**  
   - Métricas: RMSE, MAPE, R² ajustado y NWRMSLE (métrica oficial de Kaggle).  
   - Comparación de predicciones vs valores reales.  

6. **Optimización**  
   - GridSearch para ajustar hiperparámetros en XGBoost.  
   - Validación cruzada para robustez.  

##  Resultados
- Los modelos lograron capturar patrones estacionales clave.  
- Se observó correlación interesante entre ventas y precio del petróleo y estacionalidades.  
- LightGBM ofreció mejor eficiencia de entrenamiento, mientras que XGBoost mostró métricas competitivas tras tuning.  

##  Conclusiones
El proyecto confirma que:  
- El **feature engineering** en series temporales (feriados, precios externos, variables de calendario) marca la diferencia.  
- Modelos de gradient boosting (XGBoost/LightGBM) son especialmente poderosos en escenarios con múltiples variables externas.  

## 🛠️ Tecnologías usadas
- Python, Pandas, NumPy  
- Matplotlib, Seaborn  
- XGBoost, LightGBM  
- Scikit-learn  

---
