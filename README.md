<div align="center">

![Banner](assets/banner.png)

# Sistema de alarma temprana y segmentación de riesgo renal

</div>

## Autores

Sol Valeria Arias Rojas, Ángel Javier Corzo Arias, Elías David Arrieta Olivero

## Objetivo

Construir un sistema de alarma temprana que estime el riesgo de enfermedad renal crónica a partir de datos clínicos de rutina e identifique los factores más asociados a ese riesgo.

## Dataset

**Chronic Kidney Disease Risk Prediction Dataset**: 50.000 pacientes sintéticos y 40 variables (demográficas, corporales, clínicas, hábitos y antecedentes), con un score y una categoría de riesgo (Low, Moderate, High).

- Descarga: https://www.kaggle.com/datasets/mobeenfatimah/chronic-kidney-disease-risk-prediction-dataset

> Los pacientes son sintéticos: los resultados no son hallazgos médicos.

## Modelos

`GaussianNB` · `Árbol de decisión` · `Random Forest` · `SVM (SVC)` · `SVR` · `Grid Search` · `Submuestreo`

## Enlaces

- 💻 Código: [notebooks/Avance_CKD.ipynb](notebooks/Avance_CKD.ipynb)
- 🎥 Video: <PEGAR_LINK_DEL_VIDEO>
- 📦 Repositorio: <PEGAR_LINK_DEL_REPOSITORIO>

---

## Estructura del repositorio

```
ckd-repo/
├── README.md
├── requirements.txt
├── .gitignore
├── assets/
│   └── banner.png          # imagen de 800 x 300
└── notebooks/
    └── Avance_CKD.ipynb    # notebook completo (Avance 1, 2 y 3)
```

## Cómo abrir y ejecutar el proyecto

### Opción A: Google Colab (la más fácil)

1. Abre el notebook en GitHub y copia su URL.
2. Entra a https://colab.research.google.com → **Archivo → Abrir cuaderno → pestaña GitHub** → pega la URL.
3. Ejecuta todo con **Entorno de ejecución → Ejecutar todo**.

El dataset se descarga automáticamente con `kagglehub`, no hay que subir ningún archivo.

### Opción B: en tu computador

```bash
git clone <PEGAR_LINK_DEL_REPOSITORIO>
cd ckd-repo
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/Avance_CKD.ipynb
```

## Contenido del notebook

1. **Avance 1:** exploración, selección de variables, calidad de datos y análisis descriptivo.
2. **Avance 2:** clasificación binaria (Alto vs. resto) y multiclase (Bajo, Moderado, Alto), curvas de aprendizaje y experimento de balanceo por submuestreo.
3. **Avance 3:** regresión del `CKD_Risk_Score` con Árbol, Random Forest y SVR.
