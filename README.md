# 🛢️ Oil Well Profitability Prediction

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)  
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Modeling-orange)  
![Status](https://img.shields.io/badge/Status-Completed-success)  
![RMSE](https://img.shields.io/badge/RMSE-37.5-yellow)  
![Profit](https://img.shields.io/badge/Profit-125M%20USD-brightgreen)  
![Risk](https://img.shields.io/badge/Risk%20of%20Loss-1.8%25-lightgrey)  


--- 
## Descripción del Proyecto
Trabajas en la compañía de extracción de petróleo **OilyGiant**. El objetivo es **encontrar la mejor región para abrir 200 nuevos pozos de petróleo**, maximizando los beneficios y minimizando los riesgos.  

El proyecto consiste en:
- Predecir el volumen de reservas en pozos nuevos con **Regresión Lineal**.  
- Seleccionar los **200 pozos más prometedores** por región.  
- Estimar beneficios esperados considerando el presupuesto.  
- Evaluar **riesgos y beneficios** usando **bootstrapping (1000 muestras)**.  
- Proponer la región más rentable con riesgo de pérdidas inferior al **2.5%**.  

---

## Dataset
Archivos disponibles:
- `geo_data_0.csv`  
- `geo_data_1.csv`  
- `geo_data_2.csv`  

Características:  
- `id` → Identificador único del pozo.  
- `f0, f1, f2` → Variables geológicas.  
- `product` → Volumen de reservas (en miles de barriles).  

---

## Metodología
1. **Preparación de datos**
   - Carga de datasets.  
   - División en entrenamiento (75%) y validación (25%).  

2. **Entrenamiento de modelos**
   - Algoritmo: **Regresión Lineal**.  
   - Evaluación con **RMSE** y volumen medio de reservas.  

3. **Selección de pozos**
   - Selección de los **200 pozos con mayor predicción** en cada región.  
   - Cálculo de ingresos:  
     - 1 barril = **4.5 USD**.  
     - 1 unidad (`product`) = **4500 USD**.  
   - Presupuesto: **100 millones USD** para 200 pozos.  

4. **Evaluación de rentabilidad**
   - Estimación de ganancias totales por región.  
   - Umbral mínimo: **111.1 unidades promedio por pozo** para evitar pérdidas.  

5. **Análisis de riesgos con bootstrapping**
   - 1000 iteraciones de muestreo.  
   - Cálculo de **beneficio medio, intervalo de confianza (95%) y riesgo de pérdidas**.  

6. **Selección final**
   - Región con **mayor beneficio esperado** y **riesgo < 2.5%**.  

---

## Resultados
- **Modelo**: Regresión Lineal  
- **RMSE (validación)**: [ejemplo: 37.5]  
- **Ganancia promedio (mejor región)**: [ejemplo: 125M USD]  
- **Intervalo de confianza (95%)**: [ejemplo: 85M – 160M USD]  
- **Riesgo de pérdidas**: [ejemplo: 1.8%] 

---

## Conclusión
- La mejor región para perforar es: **[especificar región seleccionada]**.  
- Se cumplen las condiciones de negocio:  
  - Rentabilidad superior al umbral.  
  - Riesgo de pérdidas < 2.5%.  
- El modelo demuestra ser útil para la **planificación estratégica de perforación petrolera**.  

---

## Tecnologías Utilizadas
- Python (pandas, numpy, scikit-learn)  
- Matplotlib / Seaborn (visualización)  
- Bootstrapping (riesgo y ganancias)  

---

## 👨‍💻 Autor  

**Gerzon Medina Ortiz**  
📧 [gerzon13medin@gmail.com](mailto:gerzon13medin@gmail.com)  
💼 [LinkedIn](https://www.linkedin.com/in/gerzon-medina-robotics-datascience)  
