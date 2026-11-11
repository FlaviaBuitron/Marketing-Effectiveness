# Predicción de contratación de depósitos a plazo

Proyecto de clasificación binaria sobre datos de campañas de marketing bancario
(telemarketing). El objetivo es predecir si un cliente contrata un depósito a plazo
(`Expected` = 1) o no (`Expected` = 0). Las clases están muy desbalanceadas (~11 % de positivos),
por lo que la métrica de referencia es el **Macro F1**.

Proyecto realizado para un concurso de Kaggle. El notebook documenta el proceso completo:
análisis exploratorio, preprocesamiento, modelos probados (KNN, árbol de decisión, Random Forest,
bagging y AdaBoost), ajuste de hiperparámetros y umbral de decisión, y generación de las submissions.

## Contenido

| Fichero | Descripción |
|---|---|
| `Marketing-Effectiveness.ipynb` | Notebook principal con todo el análisis y los modelos |

## Datos

Los datos **no están incluidos** en este repositorio porque pertenecen al concurso de Kaggle.
Para ejecutar el notebook, descárgalos desde la página de la competición y colócalos en la
raíz del proyecto con estos nombres:

- `train.csv`
- `test_nolabel.csv`
- `sample_submission.csv`

## Requisitos

- Python 3.10 o superior
- pandas, numpy, matplotlib, seaborn, scipy, scikit-learn
- jupyter (o usar VS Code / Google Colab)

Instalación rápida:

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
```

## Cómo ejecutarlo

1. Coloca los CSV en la carpeta del proyecto (ver apartado anterior).
2. Abre el notebook:
   ```bash
   jupyter notebook Marketing-Effectiveness.ipynb
   ```
3. Ejecuta las celdas en orden (`Kernel > Restart & Run All`).

El notebook fija `np.random.seed(42)`, así que los resultados deberían ser reproducibles.

## Resultados

Las mejores submissions se obtuvieron con un árbol de decisión con ajuste del umbral de decisión
y con un Random Forest optimizado. Las puntuaciones exactas, con el detalle de cada experimento,
están en las conclusiones del notebook.
