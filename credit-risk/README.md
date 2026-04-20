# Credit Risk - Deep Learning Workspace

Repositorio de trabajo para el desarrollo del proyecto de riesgo de credito sobre LendingClub.

Este directorio concentra notebooks, datos y reportes de varias fases del proyecto. El objetivo es mantener trazabilidad tecnica de lo que ya esta implementado y dejar una base clara para continuar iterando.

## Estado actual

- Implementado:
  - `credit_risk_baseline.ipynb` (fase base)
  - `credit_risk_benchmark.ipynb` (benchmark de modelos)
  - `credit_risk_lightgbm.ipynb` (fase 3 original)
  - `credit_risk_lightgbm_fixed.ipynb` (version corregida)
- Datos disponibles en `data/`:
  - `accepted_2007_to_2018Q4.csv.gz`
  - `CPIAUCSL.csv`
  - `FEDFUNDS.csv`
  - `UNRATE.csv`
- Reportes exportados en `docs/`:
  - `credit_risk_baseline.pdf`
  - `credit_risk_benchmark.pdf`
  - `credit_risk_lightgbm_fixed.pdf`
  - `credit_risk_report.pdf`
  - `credit_risk_rf.pdf`

## Estructura

```text
credit-risk/
|-- credit_risk_baseline.ipynb
|-- credit_risk_benchmark.ipynb
|-- credit_risk_lightgbm.ipynb
|-- credit_risk_lightgbm_fixed.ipynb
|-- data/
|   |-- accepted_2007_to_2018Q4.csv.gz
|   |-- CPIAUCSL.csv
|   |-- FEDFUNDS.csv
|   `-- UNRATE.csv
|-- docs/
|   |-- credit_risk_baseline.pdf
|   |-- credit_risk_benchmark.pdf
|   |-- credit_risk_lightgbm_fixed.pdf
|   |-- credit_risk_report.pdf
|   `-- credit_risk_rf.pdf
|-- README.md
`-- requirements.txt
```

## Flujo del proyecto por fases

### Fase 1 - Baseline (`credit_risk_baseline.ipynb`)

- Carga datos crudos de LendingClub con seleccion de columnas.
- Define y limpia `target` a partir de `loan_status`.
- Aplica ingenieria temporal e inyeccion macroeconomica (FRED).
- Entrena baseline de regresion logistica.
- Genera artefactos para fases posteriores en `data/processed/`:
  - `X_train.csv`
  - `X_test.csv`
  - `y_train.csv`
  - `y_test.csv`
- Genera visualizaciones en `outputs/` (ejemplos detectados):
  - `correlacion.png`
  - `eda_exploratorio.png`
  - `dashboard_baseline.png`
  - `coeficientes_completos.png`

### Fase 2 - Benchmark (`credit_risk_benchmark.ipynb`)

- Consume `data/processed/` generado en la fase 1.
- Compara Random Forest vs MLP con estrategia de tuning sobre submuestra estratificada.
- Evalua sobre test completo y analiza trade-off de umbral.
- Genera visualizaciones en `outputs/` (ejemplos detectados):
  - `rf_feature_importance.png`
  - `threshold_optimization.png`
  - `dashboard_comparativo.png`

### Fase 3 - LightGBM original (`credit_risk_lightgbm.ipynb`)

- Replantea el pipeline con LightGBM + feature engineering avanzado.
- Incluye explicabilidad con SHAP.
- Parte de datos crudos y vuelve a construir el flujo de modelado.

### Fase 3 (corregida) - LightGBM fixed (`credit_risk_lightgbm_fixed.ipynb`)

- Version corregida con cambios metodologicos respecto a la fase 3 original.
- Incluye split Out-Of-Time, objective de coste de negocio y ajuste de variables macro con lag.
- Genera salidas en `outputs/` (ejemplos detectados):
  - `fairness_by_state.csv`
  - `shap_summary_v2.png`
  - `shap_importance_v2.png`
  - `shap_waterfall_v2.png`

## Configuracion del entorno

Desde la raiz del repositorio (`DeepLearning/`), en PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r .\credit-risk\requirements.txt
```

## Ejecucion

Abrir cualquiera de los notebooks de `credit-risk/` con Jupyter o DataSpell.

Ejemplo con Jupyter Notebook:

```powershell
jupyter notebook .\credit-risk\credit_risk_baseline.ipynb
```

Orden recomendado de ejecucion:

1. `credit_risk_baseline.ipynb`
2. `credit_risk_benchmark.ipynb`
3. `credit_risk_lightgbm.ipynb`
4. `credit_risk_lightgbm_fixed.ipynb`

## Dependencias

Las dependencias del proyecto se gestionan en `requirements.txt` dentro de esta carpeta.

## Pendiente / template para siguientes iteraciones

- Objetivo de negocio final (version cerrada): `[Pendiente]`
- Metricas objetivo de despliegue: `[Pendiente]`
- Estrategia de validacion final: `[Pendiente]`
- Registro de experimentos y cambios de version: `[Pendiente]`
- Plan de productivizacion (batch/API, monitorizacion, drift): `[Pendiente]`
- Checklist de cumplimiento y fairness para produccion: `[Pendiente]`

