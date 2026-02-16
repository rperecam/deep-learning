# Deep Learning – Prácticas del Grado en Ingeniería de Datos e Inteligencia Artificial (UAX)

Este repositorio reúne distintas prácticas, ejercicios y pequeños proyectos relacionados con **redes neuronales**, **arquitecturas de Deep Learning** y **aprendizaje automático avanzado**, desarrollados en el contexto del Grado en Ingeniería de Datos e Inteligencia Artificial de la Universidad Alfonso X el Sabio (UAX). La idea es tener en un mismo sitio todo el material técnico que va surgiendo en las asignaturas del grado, de forma ordenada y fácil de consultar, tanto para uso personal como para posibles revisiones en el futuro.

El repositorio está vivo: se irá ampliando a medida que aparezcan nuevas tareas, proyectos o experimentos con MLP, CNN, RNN, Transformers y otras arquitecturas. Este documento solo pretende dar una visión general y un punto de partida para navegar por las carpetas.

---

## Estructura general del repositorio

El contenido se organiza por carpetas, normalmente una por práctica o tema. Desde aquí puedes hacerte una idea rápida de qué hay en cada sitio y entrar en más detalle cuando lo necesites. A medida que se añadan nuevas prácticas, este índice se actualizará con una breve descripción de cada una.

```
DeepLearning/
├── README.md
├── CHANGELOG.md
```

### Prácticas y proyectos

> **Nota:** Esta sección se actualizará conforme se añadan nuevas prácticas. De momento, el repositorio está preparado con la estructura base para comenzar a trabajar.

<!-- Template para futuras prácticas:
#### nombre-practica/ – Título descriptivo de la práctica
Breve descripción del objetivo y alcance de la práctica.

**Características principales:**
- Arquitectura utilizada: [MLP/CNN/RNN/Transformer/etc.]
- Dataset: [nombre del dataset]
- Técnicas aplicadas: [regularización, data augmentation, transfer learning, etc.]
- Métricas: [accuracy, F1-score, loss, etc.]
- Herramientas: [PyTorch/TensorFlow/Keras + librerías específicas]
-->

---

## Cómo trabajar con este repositorio

La idea es que este repositorio funcione como un cuaderno de trabajo a largo plazo. Lo normal será clonar el repositorio en tu entorno de desarrollo (por ejemplo, **DataSpell**), entrar en la carpeta de la práctica que quieras revisar y seguir las instrucciones específicas de esa carpeta (si tiene su propio `README.md`) o simplemente abrir los notebooks y scripts relevantes.

En un flujo típico con Python podrías:

1. Crear y activar un entorno virtual (o Conda) en la raíz del repositorio.
2. Instalar las dependencias indicadas por cada práctica (por ejemplo, usando `requirements.txt`).
3. Abrir el cuaderno Jupyter o ejecutar los scripts que acompañan a la práctica.

Por ejemplo, en **PowerShell**, situándote en la raíz del repositorio:

```powershell
# Opción 1: Entorno virtual con venv
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt

# Opción 2: Entorno Conda (recomendado para Deep Learning)
conda create -n deeplearning python=3.10
conda activate deeplearning
pip install torch torchvision numpy pandas matplotlib seaborn scikit-learn jupyter

# Abrir Jupyter o DataSpell
jupyter notebook .\notebooks\tu_notebook.ipynb
```

A partir de ahí, cada carpeta podrá tener sus propias instrucciones adicionales, dependencias concretas (por ejemplo, versiones específicas de PyTorch para GPU) o notas técnicas sobre hiperparámetros y resultados experimentales.

---

## Mantener el repositorio al día

Aunque está pensado principalmente para uso personal durante el grado, es útil mantener una mínima estructura para que el repositorio siga siendo claro con el paso del tiempo. Algunas ideas sencillas:

- **Cada vez que se cree una nueva práctica o proyecto**, añadir una carpeta con un nombre descriptivo y, si es posible, un pequeño `README.md` dentro explicando el objetivo, la arquitectura implementada y cómo ejecutar el código.

- **Actualizar este `README.md` principal** cuando se añadan carpetas nuevas que merezcan aparecer en el índice, sumando una breve descripción similar al template proporcionado arriba.

- **Mantener al día los archivos de requisitos** (`requirements.txt`, entornos de conda, etc.) para poder reconstruir los entornos sin demasiadas sorpresas cuando se retomen las prácticas más adelante. Esto es especialmente importante en Deep Learning donde las versiones de PyTorch/TensorFlow y CUDA pueden causar incompatibilidades.

- **Anotar cualquier decisión técnica relevante** o problemas encontrados:
  - Versiones conflictivas de librerías (PyTorch + CUDA, TensorFlow GPU)
  - Hiperparámetros que funcionaron bien o mal
  - Problemas de overfitting/underfitting y cómo se resolvieron
  - Tiempos de entrenamiento y configuración de hardware (GPU/CPU)
  - Mejoras pendientes o experimentos futuros

- **Documentar resultados experimentales** en la carpeta `results/` con gráficas de loss/accuracy, matrices de confusión y checkpoints de modelos entrenados.

- **Usar `CHANGELOG.md`** para llevar un registro cronológico de cambios importantes (ver archivo en la raíz del repositorio).

---

## Documentación técnica

Este proyecto incluye un sistema de documentación completo:

- **`CHANGELOG.md`**: Registro de cambios siguiendo el estándar "Keep a Changelog"
- **`docs/memoria_tecnica.md`**: Template para memorias técnicas con secciones de metodología, resultados y análisis
- **Docstrings**: Formato Google Style en todas las funciones y clases
- **`.gitignore`**: Configurado para excluir checkpoints pesados, datasets grandes y archivos temporales

---

## Tecnologías y herramientas

- **Lenguaje**: Python 3.10+
- **Frameworks DL**: PyTorch, TensorFlow/Keras (según la práctica)
- **Librerías científicas**: NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn
- **Entorno de desarrollo**: DataSpell (JetBrains) con soporte para Jupyter
- **Control de versiones**: Git
- **Gestión de entornos**: Conda / venv

---

Con el tiempo, la intención es que este repositorio se convierta en una especie de **resumen práctico de las asignaturas de Deep Learning y aprendizaje automático** dentro del Grado en Ingeniería de Datos e Inteligencia Artificial (UAX): un sitio donde vuelvas cuando quieras recordar cómo resolviste una práctica, reutilizar código de arquitecturas neuronales o enseñar tu trabajo técnico en este ámbito.

---

**Última actualización**: 2026-02-16  
**Autor**: Rodrigo Pérez Campesino
**Asistente técnico**: Anne (Deep Learning Copilot)


