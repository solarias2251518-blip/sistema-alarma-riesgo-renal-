<div align="center">

# Sistema de alarma temprana de riesgo renal

![Banner](assets/banner.png)

</div>

## Autores

Sol Valeria Arias Rojas, Ángel Javier Corzo Arias, Elías David Arrieta Olivero 

## Objetivo

Construir un sistema de alarma temprana que estime el riesgo de enfermedad renal crónica a partir de datos clínicos de rutina e identifique los factores más asociados a ese riesgo.

## Dataset

**Chronic Kidney Disease Risk Prediction Dataset** (Kaggle): 50.000 pacientes sintéticos y 40 variables demográficas, clínicas, de hábitos y antecedentes, con un puntaje de riesgo (`CKD_Risk_Score`, de 9 a 100) y una categoría de riesgo (`CKD_Risk`: Low, Moderate, High).

- Descarga: https://www.kaggle.com/datasets/mobeenfatimah/chronic-kidney-disease-risk-prediction-dataset

De las 40 variables, en el análisis exploratorio se seleccionaron las 10 más relacionadas con el riesgo:

| Variable | Descripción |
| --- | --- |
| `eGFR` | Tasa de filtración glomerular estimada [mL/min/1,73 m²] |
| `Serum_Creatinine` | Creatinina sérica [mg/dL] |
| `Age` | Edad del paciente [años] |
| `Blood_Urea` | Urea en sangre [mg/dL] |
| `Blood_Pressure_Systolic` | Presión arterial sistólica [mm Hg] |
| `Albumin` | Albúmina sérica [g/dL] |
| `Hypertension` | Hipertensión [Yes / No] |
| `Diabetes` | Diabetes [Yes / No] |
| `Family_History_CKD` | Antecedentes familiares de enfermedad renal crónica [Yes / No] |
| `Smoking_Status` | Tabaquismo [Never / Former / Current] |
| **`CKD_Risk`** | Variable objetivo de clasificación [Low / Moderate / High] |
| **`CKD_Risk_Score`** | Variable objetivo de regresión [9 – 100] |


> Los pacientes son sintéticos: los resultados no son hallazgos médicos.

## Modelos

### Supervisados

- Gaussian Naive Bayes (Classifier)
- Decision Tree (Classifier, Regressor)
- Random Forest (Classifier, Regressor)
- Support Vector Machine (Classifier, Regressor)

## Enlaces

-  Código: [notebooks/Avance_CKD.ipynb](notebooks/Avance_CKD.ipynb)
-  Video: <PEGAR_LINK_DEL_VIDEO>
-  Repositorio: https://github.com/solarias2251518-blip/sistema-alarma-riesgo-renal-

---

## Estructura del repositorio

```
sistema-alarma-riesgo-renal-/
├── README.md
├── requirements.txt
├── .gitignore
├── assets/
│   └── banner.png          
└── notebooks/
    └── Avance_CKD.ipynb   
```

## Cómo abrir y ejecutar el proyecto

### Opción A: Google Colab 

1. Abre el notebook en GitHub y copia su URL.
2. Entra a https://colab.research.google.com → **Archivo → Abrir cuaderno → pestaña GitHub** → pega la URL.
3. Ejecuta todo con **Entorno de ejecución → Ejecutar todo**.

El dataset se descarga automáticamente con `kagglehub`, no hay que subir ningún archivo.

### Opción B: en tu computador

```bash
git clone https://github.com/solarias2251518-blip/sistema-alarma-riesgo-renal-.git
cd sistema-alarma-riesgo-renal-
python -m venv venv
source venv/bin/activate        # En Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/Avance_CKD.ipynb
```

## Contenido del notebook

1. **Avance 1:** exploración, selección de variables, calidad de datos y análisis descriptivo.
2. **Avance 2:** clasificación binaria (Alto vs. resto) y multiclase (Bajo, Moderado, Alto), curvas de aprendizaje y experimento de balanceo por submuestreo.
3. **Avance 3:** regresión del `CKD_Risk_Score` con Árbol, Random Forest y SVR.
