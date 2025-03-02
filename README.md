# Cancer Mortality Regression

## Descripción  
Este proyecto realiza un **análisis de regresión** para predecir la **tasa de mortalidad por cáncer** en condados de EE.UU. Se utilizan distintos modelos de regresión lineal en **R**, evaluando variables individuales y una componente principal obtenida mediante **Análisis de Componentes Principales (PCA)**.

## Tecnologías utilizadas  
- **R** (ggplot2, reshape2, broom, lmtest, tidyr, vioplot)  
- **Regresión lineal** para modelado predictivo  
- **Análisis de Componentes Principales (PCA)**  
- **Métricas de evaluación**: R², RMSE y MAE  

## Cómo ejecutar el análisis  
1. Clonar este repositorio:  
   ```sh
   git clone https://github.com/Nico9874/cancer-mortality-regression.git

## Resultados clave  
Se compararon tres modelos de regresión utilizando diferentes variables predictoras para estimar la tasa de mortalidad por cáncer (`target_deathrate`).  

| Variable predictora      | R²   | RMSE  | MAE  |
|-------------------------|------|------|------|
| `pctbachdeg25_over`     | 0.213 | 26.21 | 19.56 |
| `pctpubliccoveragealone` | 0.166 | 26.94 | 19.85 |
| `PCA_Component_1`       | **0.229** | **25.94** | **19.10** |

### **Conclusión:**  
✅ El modelo basado en PCA_Component_1 es la mejor opción inicial, ya que presenta el mayor R² (0.23) y los menores errores (RMSE: 25.94, MAE: 19.10).
📌 Sin embargo, el ajuste sigue siendo limitado. Se recomienda probar con más variables o explorar modelos más avanzados (regresión múltiple, machine learning) para mejorar la precisión.
