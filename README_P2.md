
# Telecom X — Parte 2 · Predicción de Churn (Versión B · Colab-only)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USER/Desafio_2_P2B/blob/main/notebooks/TelecomX_P2_colab_v2.ipynb)

**Esta versión B** introduce diferencias claras respecto de la versión anterior: *feature engineering* adicional, validación **repetida** (5×2), selección de **calibración por Brier score** y doble criterio de **umbral de negocio** (máxima ganancia y no-pérdida).

## 🎯 Objetivo
Anticipar clientes con mayor riesgo de **churn** y priorizar acciones para maximizar **ganancia neta**.

## 📁 Estructura
```
TelecomX_P2_repo_v2/
├─ README_P2_v2.md
├─ notebooks/
│  └─ TelecomX_P2_colab_v2.ipynb
├─ data/
│  └─ df_limpo.csv           # opcional si versionas datos
└─ reports/
   ├─ README_REPORT_P2_v2.md
   ├─ metrics_p2_v2.json
   └─ clientes_en_riesgo_topN_p2_v2.csv
```

## 🔧 Diferencias clave (vs. versión A)
- **Feature engineering**: `has_fiber`, `tenure_bin`, `charges_ratio`.
- **Validación**: `RepeatedStratifiedKFold (5×2)` y selección por **PR-AUC**.
- **Calibración**: isotónica o Platt, elegida por **Brier score** más bajo.
- **Umbral**: (1) **máxima ganancia** y (2) **no-pérdida**.
- Parámetros de negocio por defecto distintos: `VALUE_RETAIN=120`, `COST_CONTACT=4`, `TOP_N=300`.

## 🛠️ Cómo ejecutar
1. Abre el badge de Colab (arriba).
2. Sube `df_limpo.csv` a `/content` o ajusta `CSV_PATH` en la primera celda.
3. Ejecuta todas las celdas. Se generan artefactos en `/content/reports`.

> Cambia `USER/Desafio_2_P2B` por el repo real de tu compañero para su badge Colab.
