# 🌧️ TFM - Predicción de Precipitación con Modelo Híbrido EEMD–LSTM–ARIMA

Este repositorio contiene el código fuente, estructura y resultados del Trabajo de Fin de Máster (TFM) en Ciencia de Datos, centrado en el desarrollo de un modelo híbrido para la predicción de series temporales de precipitación mensual, aplicando descomposición EEMD, redes neuronales LSTM y modelos estadísticos ARIMA.

## 📂 Estructura de Carpetas

| Carpeta                                      | Ruta relativa (desde `BASE_DIR`)                          | Propósito principal                                                              |
|---------------------------------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------|
| `datos`                                      | `/datos`                                                  | Contiene el archivo CSV original con los datos de precipitación                 |
| `lstm_models`                                | `/modelos/lstm`                                           | Almacena los modelos LSTM entrenados por estación y componente                  |
| `arima_models`                               | `/modelos/arima`                                          | Almacena los modelos ARIMA entrenados por estación y componente                 |
| `stats_train`                                | `/estadisticas/eemd/train`                                | Métricas y entropías calculadas en el conjunto de entrenamiento                 |
| `stats_test`                                 | `/estadisticas/eemd/test`                                 | Métricas y entropías en el conjunto de prueba                                   |
| `graficos_eda`                               | `/graficas/exploratorio`                                  | Gráficas exploratorias iniciales por estación                                   |
| `graficos_eemd`                              | `/graficas/eemd`                                          | Gráficas de la descomposición EEMD por estación                                 |
| `graficos_train_mse`                         | `/graficas/resultados_modelo/train/curvas_mse`            | Curvas de error MSE por época durante el entrenamiento de LSTM                  |
| `graficos_train_dispersion`                  | `/graficas/resultados_modelo/train/dispersion`            | Gráficos de dispersión (predicción vs. real) para entrenamiento                 |
| `graficos_train_reconstruccion`              | `/graficas/resultados_modelo/train/reconstruccion`        | Reconstrucciones híbridas finales en entrenamiento                              |
| `graficos_test_dispersion`                   | `/graficas/resultados_modelo/test/dispersion`             | Gráficos de dispersión (predicción vs. real) para prueba                        |
| `graficos_test_reconstruccion`               | `/graficas/resultados_modelo/test/reconstruccion`         | Reconstrucciones híbridas finales en conjunto de prueba                         |
| `predicciones_futuras`                       | `/predicciones/futuro`                                    | Resultados de las predicciones a futuro (hasta 35 meses) por estación           |

## ⚙️ Requisitos

Este proyecto fue desarrollado en Google Colab y/o entorno local con Python 3.11. Las principales bibliotecas utilizadas son:

- `numpy`, `pandas`
- `matplotlib`, `seaborn`
- `PyEMD`
- `tensorflow`
- `statsmodels`
- `scikit-learn`
- `antropy`

### Instalación

En Google Colab solo es necesario instalar:

```python
!pip install EMD-signal antropy --quiet
