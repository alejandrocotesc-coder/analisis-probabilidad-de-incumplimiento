# Probabilidad de incumplimiento de cinco emisores de energía en Colombia

ISA, ISAGEN, EPM, Celsia y Enel Colombia. Periodo 2015-2025.

Prueba técnica para la práctica 2027-1, Dirección Mercado de Deuda y Capital, Bancolombia.
Alejandro Cotes, Economía y Administración de Empresas, Universidad de los Andes.

## Video

https://github.com/user-attachments/assets/d9f22318-4a11-4029-a2dd-890f54697eff

El video se puede encontrar con una mejor resolucion entrando al siguiente enlace:
[`video-presentacion.mp4`](video-presentacion.mp4). Las diapositivas son
[`Presentacion_Prueba_Bancolombia.pptx`](Presentacion_Prueba_Bancolombia.pptx), en esta misma carpeta.

## Qué se hizo

Estimé la probabilidad de incumplimiento a un año de los cinco emisores partiendo de sus
estados financieros XBRL de la Superintendencia Financiera, no de datos ya procesados.

El trabajo tiene tres partes:

1. Análisis histórico de once años: apalancamiento, cobertura de intereses y liquidez.
2. Probabilidad de incumplimiento con el scorecard de S&P Global Ratings, contrastado con el
   modelo Z de Altman.
3. Prueba de estrés sobre 2025 y correlaciones entre los indicadores.

Todos los umbrales, pesos y matrices vienen de metodologías publicadas. Las fuentes están
listadas al final. El detalle de cada puntaje cualitativo del perfil de negocio, emisor por
emisor, está en [`docs/perfil_negocio_fuentes.md`](docs/perfil_negocio_fuentes.md).

## Resultados (cifras a diciembre de 2025)

| Emisor | Deuda/EBITDA | Cobertura | Perfil financiero | Perfil de negocio | Clasificación | PD S&P | Altman Z''-EM | PD Altman |
|---|---|---|---|---|---|---|---|---|
| ENEL | 0,34x | 5,1x | 2 modesto | fuerte | a+ / a | 0,2% | 5,75 (BBB) | 0,5% |
| EPM | 2,61x | 3,5x | 3 intermedio | satisfactorio | bbb / bbb- | 0,5% | 6,19 (A-) | 0,2% |
| ISA | 4,27x | 3,2x | 4 significativo | satisfactorio | bbb- / bb+ | 0,5% | 5,43 (BB) | 2,2% |
| ISAGEN | 3,65x | 1,7x | 5 agresivo | razonable | bb- | 2,2% | 4,79 (B+) | 5,5% |
| CELSIA | 3,11x | 2,4x | 4 significativo | débil | bb- | 2,2% | 4,03 (B) | 5,5% |

Las probabilidades a un año quedan así con el scorecard de S&P: Enel 0,2%, EPM e ISA 0,5%, ISAGEN y
Celsia 2,2%. Con Altman: EPM 0,2%, Enel 0,5%, ISA 2,2%, ISAGEN y Celsia 5,5%. Son tasas anuales, no
acumuladas. El 2,2% de ISAGEN quiere decir que, históricamente, cerca de una de cada cuarenta y cinco
empresas con esa clasificación incumplió dentro del año siguiente, contra una de cada quinientas en el
caso de Enel.

La frontera relevante está en bbb-, donde termina el grado de inversión. Enel y EPM quedan por encima
con los dos métodos. ISA queda justo en el borde con S&P, bbb- / bb+, y por debajo con Altman, BB.
ISAGEN y Celsia quedan en grado especulativo, bb-, y son las dos últimas con los dos modelos. La
distancia entre el primero y el último es de once veces con S&P y de más de veinticinco con Altman.

Dos advertencias sobre estos números. El nivel absoluto sale de tablas de incumplimiento histórico
global, no colombiano, así que se lee como orden de magnitud y no como pronóstico; el orden entre los
cinco sí sale de sus propias cifras. Y falta el paso 5 de la metodología de S&P, el tope por riesgo
soberano, que solo podría bajar las clasificaciones y nunca subirlas, así que estas probabilidades son
un piso.

Tres cosas que salieron del análisis:

ISA es la más endeudada del grupo con 4,27 veces EBITDA y aun así queda tercera en riesgo, con 0,5%
contra 2,2% de ISAGEN y Celsia. Su
deuda es la más barata de las cinco y su negocio es transmisión regulada, así que el
apalancamiento por sí solo daría un orden distinto al que da el scorecard completo.

ISA y Celsia tienen el mismo perfil financiero, nivel 4, y terminan a dos escalones de
distancia en la clasificación. La diferencia está en el perfil de negocio: transmisión regulada
con ingresos por contrato contra generación expuesta al clima. La volatilidad del margen EBITDA
de Celsia es 26,6% contra un umbral sectorial de 21%, la más alta de las cinco. Si se supone el
mismo perfil de negocio para todos los emisores, que es lo habitual al replicar esta
metodología, esa diferencia desaparece.

S&P y Altman dan el mismo orden salvo en los dos primeros puestos, pese a usar insumos
distintos: uno mide flujo y el otro estructura de balance. Donde más discrepan es en ISA, a la
que Altman asigna cuatro veces más probabilidad porque sus utilidades retenidas son pequeñas
frente al activo.

## Cómo reproducirlo

1. Descomprimir los cinco archivos de [`data/xbrl/`](data/xbrl) en carpetas con el nombre de cada emisor.
   Son los 55 estados financieros anuales consolidados del SIMEV / RNVE.
2. Instalar dependencias: `pip install -r requirements.txt`
3. Correr [`notebooks/01_extraccion_xbrl.ipynb`](notebooks/01_extraccion_xbrl.ipynb) y después
   [`notebooks/02_analisis_ratios.ipynb`](notebooks/02_analisis_ratios.ipynb),
   en ese orden. Hay que ajustar la variable `RUTA` de cada uno a la carpeta de datos.

Los notebooks están escritos para Google Colab y montan Drive en la primera celda. Para
correrlos localmente basta con borrar esa celda.

Los CSV de [`data/procesada/`](data/procesada) y las figuras de [`figuras/`](figuras) se generan solos.

## Notas sobre la extracción

El lector de XBRL es propio. Arelle, que es la vía estándar, falló porque el servidor de la
Superfinanciera no entregaba la taxonomía. El notebook 01 lee el XML directo con lxml y resuelve
varias diferencias entre emisores: elige los contextos por fecha y no por nombre, porque cada
emisor los nombra distinto; detecta la escala automáticamente (pesos o miles de pesos); y tiene
cuentas alternativas para las cifras que no todos reportan con la misma etiqueta.

Los controles de calidad detectaron partidas mal etiquetadas en el XBRL de dos emisores, que el
notebook corrige con las cifras de sus propias notas, y un ingreso extraordinario de ISA en 2016
(RBSE, 5,5 billones) que se resta porque de otro modo distorsiona la serie completa.

Dos cosas que se descartaron: estimar un modelo propio de default sobre esta muestra, porque con
cinco emisores y cero incumplimientos no hay con qué estimarlo; y la PD implícita en spreads de
mercado, porque los bonos de estos emisores son ilíquidos. Altman sí se aplica porque sus
coeficientes están publicados.

## Limitaciones

- La clasificación no es una calificación. Falta el paso 5 de la metodología de S&P, el tope por
  riesgo soberano, que requiere un juicio sobre la posición del emisor frente al soberano.
- Las probabilidades son tasas de default históricas globales, no colombianas.
- Los umbrales de S&P son globales y se aplican a emisores endeudados a tasas colombianas.
- Ningún emisor revela sus líneas de crédito comprometidas, que S&P cuenta como fuentes de
  liquidez. La prueba de liquidez se reporta aparte y no como tope sobre la clasificación.
- No se aplicaron los ajustes cualitativos de Altman por riesgo soberano y moneda. El autor los
  describe pero no los tabula en número de escalones.
- ISAGEN reporta estados individuales hasta 2022 y consolidados desde 2023.

Las dos primeras omisiones van en la misma dirección, así que estos resultados subestiman el
riesgo antes que exagerarlo.

## Estructura

```
video-presentacion.mp4              el video, 6:19
Presentacion_Prueba_Bancolombia.pptx las diapositivas
notebooks/                          extracción y análisis
data/xbrl/                          los 55 estados financieros, un ZIP por emisor
data/procesada/                     tablas que generan los notebooks
figuras/                            figuras que generan los notebooks
docs/                               justificación del perfil de negocio con fuentes
```

## Fuentes

Datos: Superintendencia Financiera de Colombia, SIMEV / RNVE, estados financieros XBRL
2015-2025.

Metodología de calificación:

- S&P Global Ratings, Corporate Methodology, 7 de enero de 2024. Tablas 1, 2, 3, 14, 15, 16, 17
  y 18. https://www.maalot.co.il/Publications/MT20240214173645.PDF
- S&P Global Ratings, Sector-Specific Corporate Methodology, 7 de julio de 2025. Pesos por
  sector y umbrales de volatilidad del margen.
- S&P Global Ratings, Methodology: Industry Risk. Puntajes de riesgo de industria.
- S&P Global Ratings, Country Risk Assessment Methodology, actualización de octubre de 2024.
- S&P Global Ratings, Methodology And Assumptions: Liquidity Descriptors For Global Corporate
  Issuers, 16 de diciembre de 2014.

Probabilidades de incumplimiento: Berk, J. y DeMarzo, P., Corporate Finance, tabla 12.2.

Modelo de Altman: Altman, E., Hartzell, J. y Peck, M. (1995), Emerging Market Corporate Bonds,
A Scoring System. Coeficientes del modelo Z'', constante de mercados emergentes y tabla de
equivalencia con calificaciones.
