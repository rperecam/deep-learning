# DeepLearning - Practicas del Grado en Ingenieria de Datos e Inteligencia Artificial (UAX)

Este repositorio centraliza practicas, ejercicios y experimentos de aprendizaje automatico y Deep Learning desarrollados durante el Grado en Ingenieria de Datos e Inteligencia Artificial de la Universidad Alfonso X el Sabio (UAX).

El objetivo es mantener en un unico sitio el material tecnico del grado, de forma ordenada y facil de consultar para:

- repasar practicas ya realizadas,
- reutilizar codigo y notebooks,
- documentar decisiones tecnicas,
- y facilitar futuras mejoras o ampliaciones.

El repositorio esta vivo y se ira ampliando conforme aparezcan nuevas practicas o proyectos.

---

## Estado actual

Actualmente hay una practica activa en el repositorio:

- `credit-risk/`: trabajo de riesgo de credito con notebooks y documentacion en PDF.

No hay, de momento, un proyecto de Deep Learning (CNN/RNN/Transformers) iniciado como carpeta independiente en la raiz.

---

## Estructura general del repositorio

```text
DeepLearning/
|- README.md
|- CHANGELOG.md
|- requirements.txt
|- credit-risk/
|  |- README.md
|  |- requirements.txt
|  |- credit_risk_baseline.ipynb
|  |- credit_risk_benchmark.ipynb
|  |- credit_risk_lightgbm.ipynb
|  |- credit_risk_lightgbm_fixed.ipynb
|  |- data/
|  |  |- accepted_2007_to_2018Q4.csv.gz
|  |  |- CPIAUCSL.csv
|  |  |- FEDFUNDS.csv
|  |  |- UNRATE.csv
|  |- docs/
|     |- credit_risk_baseline.pdf
|     |- credit_risk_benchmark.pdf
|     |- credit_risk_lightgbm_fixed.pdf
|     |- credit_risk_report.pdf
|     |- credit_risk_rf.pdf
```

---

## Proyecto activo: `credit-risk/`

Esta carpeta contiene la practica de riesgo de credito con:

- notebooks de trabajo y comparativas,
- datos tabulares y series macroeconomicas,
- documentacion en PDF generada durante la practica.

Notebooks disponibles:

- `credit-risk/credit_risk_baseline.ipynb`
- `credit-risk/credit_risk_benchmark.ipynb`
- `credit-risk/credit_risk_lightgbm.ipynb`
- `credit-risk/credit_risk_lightgbm_fixed.ipynb`

---

## Como trabajar con este repositorio

Flujo recomendado en Windows PowerShell, desde la raiz `DeepLearning/`:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter notebook .\credit-risk\credit_risk_baseline.ipynb
```

Notas:

- cada carpeta de practica puede tener dependencias propias,
- si una practica incluye su propio `requirements.txt`, prioriza ese archivo,
- en `credit-risk/` existe `requirements.txt`, pero actualmente no define dependencias especificas.

---

## Convencion para nuevas practicas (template)

Cuando se anada una nueva practica, usar una carpeta dedicada y documentar lo minimo necesario.

Template sugerido:

```text
nombre-practica/
|- README.md
|- requirements.txt
|- notebooks/
|- src/
|- data/
|- docs/
|- results/
```

Template de `README.md` para cada practica:

```markdown
# Nombre de la practica

## Objetivo
[Pendiente]

## Dataset
[Pendiente]

## Enfoque/modelos
[Pendiente]

## Como ejecutar
[Pendiente]

## Resultados
[Pendiente]

## Mejoras futuras
[Pendiente]
```

---

## Mantenimiento del repositorio

Para mantener el repositorio claro a largo plazo:

- actualizar este `README.md` cuando se cree una carpeta nueva,
- mantener `requirements.txt` al dia (raiz y subcarpetas),
- registrar cambios relevantes en `CHANGELOG.md`,
- anotar problemas de versiones o decisiones tecnicas en cada practica.

---

## Roadmap (pendiente)

Seccion reservada para futuras practicas de Deep Learning.

- [ ] Practica DL 01 - [Pendiente de definir]
- [ ] Practica DL 02 - [Pendiente de definir]
- [ ] Proyecto final DL - [Pendiente de definir]

---

## Autor

- Rodrigo Perez Campesino

Ultima actualizacion: 2026-04-20


