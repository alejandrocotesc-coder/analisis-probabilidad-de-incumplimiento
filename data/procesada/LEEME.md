# Datos procesados

Esta carpeta se llena sola al correr los notebooks, en este orden:

| Archivo | Lo genera | Contenido |
|---|---|---|
| `tabla_emisores.csv` | notebook 01 | 55 filas (5 emisores × 11 años) con las cifras extraídas de los XBRL |
| `ratios_emisores.csv` | notebook 02 | la tabla anterior más todos los ratios, perfiles, clasificaciones y PD |
| `liquidez_2025.csv` | notebook 02 | prueba de liquidez de S&P para 2025, con sensibilidades |
| `estres_2025.csv` | notebook 02 | prueba de estrés, cuatro escenarios |
| `altman_2025.csv` | notebook 02 | modelo Z de Altman para 2025 |
| `resumen_2025.csv` | notebook 02 | consolidado final por emisor |

Las cifras están en **billones de pesos colombianos**.
