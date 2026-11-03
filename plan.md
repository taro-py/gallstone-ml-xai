# Proyecto de Clasificación y Explicabilidad Clínica (XAI): Litiasis Biliar

Este repositorio contiene el desarrollo del proyecto de Machine Learning y Explicabilidad Clínica (XAI) enfocado en la predicción de litiasis biliar utilizando el dataset **UCI Gallstone-1** (319 pacientes, 38 características).

---

## 👥 División de Roles y Responsabilidades

### 🛠️ Miembro 1: Líder de Código y Modelado ML
**Responsabilidad principal:** Procesamiento del dataset y construcción/evaluación de los modelos de clasificación.

* **Carga y Análisis Exploratorio de Datos (EDA):** Cargar el dataset `gallstone-1` de UCI y analizar la distribución de variables demográficas, bioimpedancia y parámetros de laboratorio.
* **Preprocesamiento y Pipeline:** 
  * Aplicar escalado de características (e.g., `StandardScaler`).
  * Dividir la muestra en entrenamiento y prueba ($80/20$ o $70/30$).
  * Implementar validación cruzada estratificada ($k$-fold).
* **Entrenamiento de Modelos:** Probar al menos 3 o 4 algoritmos de clasificación (e.g., Regresión Logística, Random Forest, XGBoost/LightGBM, SVM).
* **Evaluación de Métricas:** Calcular e interpretar métricas clave: *Accuracy*, *Precision*, *Recall*, *F1-score*, *ROC-AUC* y matriz de confusión.
* **Entrega:** Mantener un código limpio, optimizado, comentado y estructurado en el Jupyter Notebook principal.

---

### 🔬 Miembro 2: Especialista en Explicabilidad (XAI) y Análisis Clínico
**Responsabilidad principal:** Aplicar técnicas de explicabilidad sobre los modelos y contrastar los resultados con el contexto médico.

* **Implementación de SHAP y LIME:**
  * Extraer valores SHAP globales (*summary plot*, *bar plot*).
  * Generar análisis locales (*waterfall plots*) para explicar predicciones individuales.
* **Identificación de Caracterizaciones Clínicas:** Determinar qué variables (e.g., grasa visceral, perfil lipídico, enzimas hepáticas AST/ALT, bioimpedancia) contribuyen significativamente al riesgo de cálculos biliares.
* **Contraste Científico:** Revisar el artículo de referencia (*MD Journal*) y comparar si los hallazgos del modelo coinciden con la literatura médica actual.
* **Entrega:** Documentar la sección de análisis e interpretación clínica directamente en el Jupyter Notebook con gráficos claros y anotados.

---

### 📄 Miembro 3: Redactor del Reporte IEEE y Diseñador de la Presentación
**Responsabilidad principal:** Consolidar el informe escrito de 2 páginas y crear la presentación ejecutiva.

* **Redacción del Reporte IEEE (Máx. 2 páginas):** Configurar la plantilla oficial IEEE en Overleaf redactando:
  * *Abstract e Introducción:* Contexto clínico y objetivo del proyecto.
  * *Metodología:* Descripción del dataset, preprocesamiento y modelos evaluados.
  * *Resultados y Explicabilidad:* Tablas de métricas y gráficos SHAP más relevantes.
  * *Discusión y Contribuciones:* Sección obligatoria detallando el aporte individual de cada integrante (Miembro 1, 2 y 3).
* **Presentación Ejecutiva (10 minutos):** Crear de 7 a 9 diapositivas visuales estructuradas para la exposición grupal.
* **Entrega Final:** Coordinar la revisión final del paquete `.zip` para la entrega a tiempo por parte del líder del grupo.

---

## ⏱️ Estructura de la Exposición (10 Minutos)

| Tiempo | Expositor | Contenido Principal |
| :--- | :--- | :--- |
| **0:00 – 3:20** | **Miembro 1** | Introducción al problema clínico de la litiasis biliar, descripción del dataset UCI (319 pacientes, 38 variables) y arquitectura de los modelos entrenados. |
| **3:20 – 6:40** | **Miembro 2** | Resultados del modelo con mayor rendimiento y análisis de explicabilidad con SHAP/LIME (variables clínicas de mayor impacto). |
| **6:40 – 10:00** | **Miembro 3** | Conclusiones principales, limitaciones del modelo, implicaciones clínicas y cierre con preguntas. |

---

## 📁 Estructura del Repositorio Sugerida

```
├── data/
│   └── gallstone-1.csv         # Dataset original de UCI
├── notebooks/
│   └── main_analysis.ipynb    # Pipeline de ML y Explicabilidad (SHAP/LIME)
├── report/
│   ├── main.tex               # Código fuente en LaTeX (Plantilla IEEE)
│   └── IEEE_Report.pdf        # Reporte consolidado de 2 páginas
├── presentation/
│   └── slides.pptx            # Diapositivas de la exposición (7-9 slides)
└── README.md                  # Guía general del proyecto
```