# analisis-ingresos
# Análisis de Edad vs Ingresos

¡Hola! Este es un proyecto simple donde analicé la relación entre la edad y los ingresos usando Python.

## Objetivo
El objetivo era entender si existe una relación entre la edad y los ingresos, y visualizar la distribución de los ingresos.

## Herramientas usadas
- **Python**: Para el análisis y visualización de datos.
- **Pandas**: Para manipular los datos.
- **Matplotlib**: Para crear gráficos.

## Código
El código utilizado es el siguiente:
```python
import pandas as pd
import matplotlib.pyplot as plt

# Crear un dataset
data = {
    'Edad': [25, 30, 35, 40, 45, 50, 55, 60, 65, 70],
    'Ingresos': [30000, 45000, 50000, 60000, 80000, 90000, 100000, 120000, 110000, 130000]
}

# Convertir el dataset en un DataFrame
df = pd.DataFrame(data)

# Mostrar las primeras filas del DataFrame
print(df)

# Calcular estadísticas básicas
print("Media de ingresos:", df['Ingresos'].mean())
print("Mediana de ingresos:", df['Ingresos'].median())
print("Desviación estándar de ingresos:", df['Ingresos'].std())

# Crear un gráfico de dispersión (edad vs ingresos)
plt.scatter(df['Edad'], df['Ingresos'], color='blue')
plt.title('Edad vs Ingresos')
plt.xlabel('Edad')
plt.ylabel('Ingresos')
plt.show()

# Crear un histograma de ingresos
plt.hist(df['Ingresos'], bins=5, color='green')
plt.title('Distribución de Ingresos')
plt.xlabel('Ingresos')
plt.ylabel('Frecuencia')
plt.show()
