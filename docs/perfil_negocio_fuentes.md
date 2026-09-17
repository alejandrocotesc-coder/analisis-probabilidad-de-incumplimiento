# Perfil de negocio emisor por emisor (paso 1 de la metodología de S&P)

Reemplaza el supuesto "perfil de negocio satisfactorio para los cinco" por una
evaluación individual. Cada puntaje tiene fuente. Lo que no se pudo verificar
está marcado como tal.

Escala de los subfactores: **1 fuerte · 2 fuerte/adecuado · 3 adecuado ·
4 adecuado/débil · 5 débil** (S&P, Corporate Methodology, 7 ene 2024).

---

## 1. Riesgo país

Tabla de S&P "Country risk assessments by group and country as of Oct. 24, 2024":
Colombia 4, Brasil 4, Perú 4, Chile 3, Panamá 4, Costa Rica 4, Guatemala 5,
El Salvador 6.

Regla (Corporate Methodology, párr. 22-26): se ponderan los países con más del
5 % de las ventas, los pesos se redondean al 5 %, el promedio se redondea al
entero, y si un país concentra 75 % o más el puntaje es el de ese país.

| Emisor | Composición de ingresos 2025 | Cálculo | Riesgo país |
|---|---|---|---|
| ISA | Brasil 43,1 % · Colombia 26,0 % · Perú 14,8 % · Chile 13,9 % | 0,45×4+0,25×4+0,15×4+0,15×3 = 3,85 | **4** |
| EPM | Colombia 73,6 % · Guatemala 10,3 % · Panamá 8,5 % | 0,75×4+0,10×5+0,10×4 = 4,1 | **4** |
| ENEL | Colombia 85,6 % | ≥75 % → Colombia | **4** |
| CELSIA | Colombia 98,6 % | ≥75 % → Colombia | **4** |
| ISAGEN | Colombia 100 % | — | **4** |

Fuentes: notas de segmentos de los estados financieros consolidados 2025
(ISA nota 32.4 p. 136; EPM nota 47.2 p. 258; Enel nota 44 p. 177;
Celsia nota 31.2; ISAGEN nota 1).

---

## 2. Riesgo de industria

S&P, "Methodology: Industry Risk", Apéndice IV, tabla 7 (republicada 7 jul 2025):

| Industria | Ciclicidad | Competencia y crecimiento | Riesgo de industria |
|---|---|---|---|
| Servicios públicos regulados | 2 bajo | 1 muy bajo | **1** |
| Generación no regulada (unregulated power and gas) | 4 | 4 | **4** |
| Infraestructura de transporte | 2 | 2 | **2** |

Regla (Corporate Methodology, párr. 27): promedio ponderado de las líneas que
pesen más de 20 % de utilidades, ingresos o activos. Se usa EBITDA por segmento.

| Emisor | Líneas > 20 % del EBITDA 2025 | Cálculo | Industria |
|---|---|---|---|
| ISA | Transmisión 81,9 % (Vías 16,9 % no llega al umbral) | 1 | **1** |
| EPM | Regulados 63,9 % · Generación 36,1 % | 0,639×1+0,361×4 = 2,08 | **2** |
| ENEL | Generación 51,4 % · Distribución 48,6 % | 0,514×4+0,486×1 = 2,54 | **3** |
| CELSIA | T&D 48 % · Generación 38 % | 0,558×1+0,442×4 = 2,33 | **2** |
| ISAGEN | Generación 100 % | 4 | **4** |

Fuentes: mismas notas de segmentos; Celsia por EBITDA de Servicios de Energía
(Presentación de resultados 4T 2025, diapositiva 17: Tx & Dx 48 %, Gx 38 %,
Cx 14 %).

Sensibilidades declaradas: ENEL queda en el borde (2,54); con ingresos daría 2
y con activos fijos 3. ISA con Vías incluida daría 1,2 → sigue en 1.

---

## 3. CICRA (tabla 1 de la Corporate Methodology)

| Emisor | País | Industria | **CICRA** |
|---|---|---|---|
| ISA | 4 | 1 | **2** |
| EPM | 4 | 2 | **3** |
| ENEL | 4 | 3 | **3** |
| CELSIA | 4 | 2 | **3** |
| ISAGEN | 4 | 4 | **4** |

---

## 4. Posición competitiva

### 4.1 Ventaja regulatoria (reguladas) / ventaja competitiva (generación)

Contexto del marco colombiano, común a las cinco:

- **Transmisión (STN)**: Resolución CREG 011 de 2009. El ingreso se remunera por
  disponibilidad de activos, no por energía transportada; las indisponibilidades
  generan compensaciones. Tasa de retorno 11,5 % real antes de impuestos
  (Res. CREG 083 de 2008), **sin revisión desde 2008**.
- **Distribución (SDL/STR)**: Resolución CREG 015 de 2018, periodo tarifario de
  5 años, esquema de ingreso máximo. WACC 12,09 % desde 2022 (Res. CREG 215 de
  2021; antes 11,36 %).
- **Riesgo de intervención política 2022-2026** (lo que más pesa):
  - Pacto por la Justicia Tarifaria (sep 2022) y Res. CREG 101-027 y 101-031 de
    2022: cambio del indexador de IPP a IPC en cargos de transmisión y
    distribución.
  - Res. MME 40225 de 2024: el Ministerio ordena a la CREG bajar en 30 días el
    costo unitario a estratos 1-3.
  - Decreto 1072 de 2025: obliga a vender en contratos al menos el 95 % de la
    generación horaria de las plantas hídricas.
  - Deuda estatal con el sector: 9,2 billones a marzo de 2026 (>3,5 bn de
    subsidios, 2,2 bn de opción tarifaria, 1,4 bn de entes territoriales);
    once meses sin pago de subsidios a noviembre de 2025. Saldo de opción
    tarifaria: 4,6 bn (2023) → 2,2-2,4 bn (2026).
  - La CREG operó sin quórum (3 de 6 comisionados) desde 2024; el quórum en
    propiedad se restableció el 29 de diciembre de 2025. Las resoluciones
    cayeron de 136 (2021) a 70 (2023).
  - S&P (ene 2025): "la autonomía de los organismos reguladores se ha debilitado
    bajo el actual gobierno, dados los cambios operativos y tarifarios mediante
    decretos del Ministerio de Minas y Energía".
  - Fitch (dic 2025): "continuous policy shifts prioritizing short-term price
    control over financial predictability are likely to erode cash flow
    visibility and place downward pressure on credit ratings".
  - Moody's (jun 2026): las condiciones crediticias de las empresas colombianas
    de energía seguirán deteriorándose al menos hasta el primer semestre de 2027.
  - Contraste histórico: S&P (2020, informe sobre ISA) llamaba al marco
    colombiano "uno de los más fuertes de la región".

| Emisor | Puntaje | Justificación |
|---|---|---|
| ISA | **2** | Transmisión remunerada por disponibilidad: sin riesgo de volumen ni de precio de la energía. Opera en cuatro jurisdicciones regulatorias (Colombia, Brasil, Perú, Chile), lo que diluye el riesgo de cualquiera. No es "fuerte" porque la tasa de retorno no se revisa desde 2008 y el indexador se cambió por resolución en 2022. |
| ENEL | **2** | Integración vertical generación + distribución (S&P la reconoce como característica fuerte). #2 en capacidad instalada y #1 en distribución. Matriz 77 % hidráulica, bajo costo variable. Descuenta: multa de la SSPD por 2.847 millones (abr 2026) por distorsión del precio en bolsa y pliego de cargos de la SIC (ago 2026). |
| EPM | **3** | Mayoría de flujos en distribución y acueducto regulados, con recuperación de costos sujeta a los retrasos del gobierno (1,3 billones adeudados a ene 2025) y a la opción tarifaria. Fitch (dic 2025): "el riesgo regulatorio de EPM es moderado". |
| CELSIA | **3** | Mismo marco que EPM. Obtuvo incentivos de calidad por 18.641 millones en 2025 (estrategia regulatoria efectiva), pero el gobierno le adeudaba 226.000 millones a ene 2025. |
| ISAGEN | **3** | 81 % de los ingresos 2025 bajo contratos (4,68 bn de 5,77 bn antes de devoluciones), lo que da protección de precio. Pero es generación pura sin integración aguas abajo y el Decreto 1072/2025 reduce su flexibilidad comercial. |

### 4.2 Escala, alcance y diversificación

| Emisor | Puntaje | Datos |
|---|---|---|
| ISA | **1** | 49.677 km de circuito y 113.365 MVA en 6 países; 64 % del STN colombiano (#1), 74 % en Perú (#1), 13 % en Chile (#2), 11 % en Brasil (#3); tres líneas de negocio (energía, vías, telecom). 2024. |
| EPM | **2** | EBITDA más grande del grupo (12,4 bn). #1 en generación del SIN (24,2 %), #2 en distribución (14,8 %) y comercialización (15,1 %), #4 en transmisión (6,41 %); 2,88 millones de clientes; multiservicio (energía, gas, agua, aguas residuales, residuos); 6 países. 2024. |
| ENEL | **2** | 4.011 MW (17,4 % del SIN, #2 en capacidad), 16,9 % de la generación; 3,96 millones de clientes y 21,6 % de la demanda nacional (#1 distribuidor); 77.415 km de red; 4 países. dic-2024. |
| CELSIA | **4** | 1,3 GW instalados y 4.386 GWh generados; >1,3 millones de clientes en Valle del Cauca y Tolima; 1,73 % del STN; 98,6 % de los ingresos en Colombia. 2025. |
| ISAGEN | **4** | 3.140 MW en 27 centrales (#3 en capacidad), 20,5 % de la demanda nacional; un solo país, un solo segmento, matriz predominantemente hidráulica. 2025. |

### 4.3 Eficiencia operativa

| Emisor | Puntaje | Datos |
|---|---|---|
| ISA | **1** | Disponibilidad de activos de uso del STN 99,93 % (2024) y >99,9 % (2025); tasa de fallas 2,88 %; compensaciones por indisponibilidad de 2.101 millones (2024) que bajan a 720 millones (2025). |
| ENEL | **2** | SAIDI 8,11 h y SAIFI 8,51 (2024); cumplió las dos metas del regulador en 2023 (ratios 0,79 y 0,97); pérdidas 7,54 % (las más bajas del grupo); disponibilidad de plantas 90,50 % (jun 2025). |
| ISAGEN | **3** | **No verificado**: no se encontró el dato de disponibilidad ni de factor de planta 2024-2025. Se asigna el valor neutro y se declara. |
| EPM | **4** | SAIDI 10,68 h, el más alto de los tres distribuidores grandes; incumplió su meta de SAIDI en 2023 (ratio 1,35); pérdidas 8,35 %. Hidroituango: sobrecostos de 12,2 billones sobre un presupuesto original de 11 billones (Contraloría, 2026), 4 de 8 unidades en operación, las restantes desplazadas a 2027-2028, multa de la SSPD de 1.817 millones por los retrasos y fallo fiscal en firme por 4,3 billones. Es el caso típico que S&P describe como "sobrecostos y retrasos" y "programa de inversión tan grande y complejo que compromete la eficiencia operativa". |
| CELSIA | **4** | Valle: SAIDI 8,48 h, incumplió meta en 2023 (ratio 1,23), pérdidas 9,14 %. Tolima: SAIDI 43,02 h y SAIFI 25,64, pérdidas 12,26 % (las más altas del grupo). Multa de la SSPD por 1.700 millones por el apagón de Sabanalarga. Compensa: disponibilidad hidráulica 93,98 %. |

### 4.4 Combinación

Perfil de grupo y pesos (Sector-Specific Corporate Methodology, jul 2025):
"National industry and utilities" 60/20/20 para los de mayoría regulada
(ISA, EPM, Celsia); "Capital or asset focus" 30/30/40 para generación y
verticalmente integrados (Enel, ISAGEN).

| Emisor | Ventaja | Escala | Eficiencia | Promedio | Posición preliminar |
|---|---|---|---|---|---|
| ISA | 2 | 1 | 1 | 1,60 | **2** |
| EPM | 3 | 2 | 4 | 3,00 | **3** |
| ENEL | 2 | 2 | 2 | 2,00 | **2** |
| CELSIA | 3 | 4 | 4 | 3,40 | **4** |
| ISAGEN | 3 | 4 | 3 | 3,30 | **4** |

---

## 5. Rentabilidad

Volatilidad = error estándar de la regresión del margen EBITDA contra el tiempo,
dividido por su promedio (Corporate Methodology, párr. 83-84), sobre los once
años 2015-2025 de nuestra tabla. Umbrales: reguladas 3/5/7/11/21 %;
generación no regulada 5/10/14/21/39 %.

Nivel: S&P excluye a las reguladas de los umbrales fijos y las compara contra
pares; para generación no regulada el umbral es margen EBITDA >30 % = por
encima del promedio. Para las distribuidoras el margen EBITDA está distorsionado
por el traslado de las compras de energía, así que se usa el ROE, como indica la
metodología.

| Emisor | SER | Volatilidad | Nivel | Base del nivel | **Rentabilidad** |
|---|---|---|---|---|---|
| ISA | 12,3 % | 5 | por encima | margen EBITDA 59,8 % (el más alto) | **4** |
| EPM | 9,4 % | 4 | promedio | ROE 11,7 % (mediana del grupo) | **4** |
| ENEL | 14,9 % | 4 | por encima | ROE 22,4 % (el más alto) | **3** |
| CELSIA | 26,6 % | 6 | por debajo | ROE 6,0 % (el más bajo) | **6** |
| ISAGEN | 15,9 % | 4 | por encima | margen EBITDA 53,8 % (>30 %) | **3** |

---

## 6. Resultado

| Emisor | Pos. comp. preliminar | Rentabilidad | Pos. competitiva | CICRA | **Perfil de negocio** |
|---|---|---|---|---|---|
| ISA | 2 | 4 | 3 | 2 | **3 satisfactorio** |
| EPM | 3 | 4 | 3 | 3 | **3 satisfactorio** |
| ENEL | 2 | 3 | 2 | 3 | **2 fuerte** |
| CELSIA | 4 | 6 | 5 | 3 | **5 débil** |
| ISAGEN | 4 | 3 | 4 | 4 | **4 razonable** |

### Efecto sobre el resultado del scorecard (2025)

| Emisor | Perfil financiero | Ancla con el supuesto | Ancla evaluada | PD |
|---|---|---|---|---|
| ISA | 4 significativo | bbb-/bb+ | **bbb-/bb+** | 0,5 % → 0,5 % |
| EPM | 3 intermedio | bbb/bbb- | **bbb/bbb-** | 0,5 % → 0,5 % |
| ENEL | 2 modesto | bbb+ | **a+/a** | 0,5 % → **0,2 %** |
| CELSIA | 4 significativo | bbb-/bb+ | **bb-** | 0,5 % → **2,2 %** |
| ISAGEN | 5 agresivo | bb | **bb-** | 2,2 % → 2,2 % |

Dos de los cinco cambian de familia de calificación: Enel sube y Celsia baja.
El ranking pasa de tener cuatro empresas empatadas en 0,5 % a tener tres
niveles: Enel (0,2 %), EPM e ISA (0,5 %), Celsia e ISAGEN (2,2 %).

---

## Limitaciones que hay que declarar

1. **El ancla no es una calificación.** Es el resultado de los dos perfiles,
   antes de los modificadores (diversificación, estructura de capital, política
   financiera, liquidez, gerencia) y antes del tope soberano. Colombia es BB-
   desde el 8 de abril de 2026, así que ninguna de estas empresas tendría en la
   práctica una calificación internacional de "a"; el ancla de Enel indica que
   su perfil autónomo es fuerte, no que S&P la calificaría así.
2. **Los subfactores son juicio.** Cada puntaje está sustentado, pero otro
   analista con las mismas fuentes podría moverlos un nivel. Los más discutibles:
   la eficiencia de ISAGEN (sin dato verificado) y la escala de Celsia.
3. **La etapa 2 de liquidez sigue igual**: solo ISA sale fuerte; los otros cuatro
   salen débiles, y sin líneas de crédito comprometidas reveladas el tope de S&P
   se reporta como sensibilidad, no como resultado.
4. **El nivel de rentabilidad de las reguladas** se comparó contra el propio
   panel de cinco empresas, no contra los retornos autorizados por la CREG, que
   no son públicos por empresa.
5. **Datos no verificados**: disponibilidad y factor de planta de ISAGEN;
   cumplimiento de metas de calidad 2024 (solo hay 2023 de la SSPD); el uso
   literal del término "regulatory advantage" por S&P para estas cinco empresas
   (los informes completos están tras muro de pago).

---

## Fuentes

Metodología
- [S&P Global Ratings, Corporate Methodology, 7 ene 2024](https://www.maalot.co.il/Publications/MT20240214173645.PDF)
- S&P Global Ratings, Sector-Specific Corporate Methodology, 7 jul 2025 (secciones 30 y 38, apéndices 2 y 3)
- [S&P Global Ratings, Methodology: Industry Risk, Apéndice IV](https://www.spglobal.com/ratings/en/regulatory/article/-/view/sourceId/8304862)
- [S&P Global Ratings, Country Risk Assessments Update: October 2024](https://spglobal.com/ratings/en/research/articles/241024-country-risk-assessments-update-october-2024-13290691)
- [S&P Global Ratings, Industry Risk Sector And Industry Variables Updated, 26 dic 2024](https://www.spglobal.com/ratings/en/regulatory/article/-/view/sourceId/13374493)

Marco regulatorio
- [Resolución CREG 011 de 2009 (transmisión)](https://normas.cra.gov.co/gestor/docs/resolucion_creg_0011_2009.htm)
- [Concepto CREG 10727 de 2013 (tasa de retorno 11,5 %)](https://gestornormativo.creg.gov.co/gestor/entorno/docs/concepto_creg_0010727_2013.htm)
- [Resolución CREG 015 de 2018 (distribución)](https://gestornormativo.creg.gov.co/gestor/entorno/docs/resolucion_creg_0015_2018.htm)
- [Resolución CREG 215 de 2021 (WACC 12,09 %)](https://gestornormativo.creg.gov.co/gestor/entorno/docs/resolucion_creg_0215_2021.htm)
- [Resolución CREG 012 de 2020 (opción tarifaria)](https://gestornormativo.creg.gov.co/gestor/entorno/docs/resolucion_creg_0012_2020.htm)
- [Resolución CREG 101-031 de 2022 (indexador IPP a IPC)](https://gestornormativo.creg.gov.co/gestor/entorno/docs/resolucion_creg_101-31_2022.htm)
- [Resolución MME 40225 de 2024](https://gestornormativo.creg.gov.co/gestor/entorno/docs/resolucion_minminas_40225_2024.htm)
- [Decreto 1072 de 2025 (95 % de generación hídrica en contratos)](https://gestornormativo.creg.gov.co/gestor/entorno/docs/decreto_1072_2025.htm)
- [MinEnergía, Pacto por la Justicia Tarifaria, sep 2022](https://minenergia.gov.co/es/sala-de-prensa/noticias-index/gobierno-petro-creg-y-empresas-llegan-a-un-acuerdo-para-la-reducci%C3%B3n-de-las-tarifas-de-energ%C3%ADa-el%C3%A9ctrica-en-el-pa%C3%ADs/)
- [Portafolio, deuda del Estado con el sector energético](https://www.portafolio.co/energia/deudas-del-gobierno-petro-y-regiones-con-el-sector-energetico-asi-se-distribuye-los-casi-10-billones-sin-pagar-490346)
- [Portafolio, subsidios adeudados por empresa, ene 2025](https://www.portafolio.co/energia/cuanto-les-debe-el-gobierno-a-las-empresas-de-energia-por-el-concepto-de-subsidios-621414)
- [Portafolio, CREG sin quórum](https://www.portafolio.co/energia/tarifas-de-energia-sin-quorum-la-creg-recibe-tarea-de-aplicar-alivios-en-30-dias-608006)
- [El Espectador, la CREG recupera quórum, dic 2025](https://www.elespectador.com/economia/con-dos-nuevas-comisionadas-la-creg-vuelve-a-contar-con-quorum-para-sesionar-noticias-hoy/)

Calificadoras
- [Portafolio, S&P sobre el sector eléctrico colombiano, ene 2025](https://www.portafolio.co/energia/los-cortos-circuitos-del-sector-electrico-colombiano-segun-s-p-global-ratings-621601)
- [Fitch, calificación de EPM, dic 2025](https://www.epm.com.co/content/dam/epm/inversionistas/informaci%C3%B3n-financiera/calificaciones-de-riesgo-crediticio/RAC_EPM_subsidiarias_2025_Informe_local_Fitch_dic.pdf)
- [Finance Colombia, Fitch sobre el Decreto 1072, dic 2025](https://www.financecolombia.com/colombias-energy-decree-raises-credit-risk-and-discourages-power-investment-says-fitch-ratings/)
- [S&P sobre Ecopetrol y Colombia BB-, 8 abr 2026](https://www.sec.gov/Archives/edgar/data/1444406/000129281426002183/ex99-1.htm)

Escala y operación
- [ISA, Reporte Integrado de Gestión 2024](https://www.isa.co/es/reporte-integrado-de-gestion-2024/)
- [ISA Intercolombia, Reporte Integrado de Gestión 2024](https://itcoasprds-a77b12eedb9aa256-endpoint.azureedge.net/blobitcoasprds4953213ea0/wp-content/uploads/2025/06/Reporte-Integrado-de-Gestion-ISA-INTERCOLOMBIA-2024.pdf)
- [EPM, Informe de Gestión 2024](https://www.epm.com.co/content/dam/epm/institucional/transparencia/rendicion-de-cuentas/rendicion-de-cuentas-2024/Informe%20de%20Gesti%C3%B3n%20EPM%20FINAL.pdf)
- [Enel Colombia, presentación corporativa FY2024](https://www.enel.com.co/content/dam/enel-co/espa%C3%B1ol/accionistas_e_inversionistas/enel-colombia/presentaciones-corporativas/2024/presentacion-corporativa-enel-colombia-fy2024.pdf)
- [Celsia, Reporte Integrado 2024](https://files.grupoargos.com/uploads-grupo-argos/2025/03/grupo-argos-reporte-integrado-celsia-2024.pdf)
- [ISAGEN, quiénes somos](https://www.isagen.com.co/Quienes-somos/)
- [XM, Informe de Operadores de Red 2024](https://sinergox.xm.com.co/infms/Operadores%20de%20Red/Informe%20Operadores%20de%20Red%20-%202024.pdf)
- [SSPD, indicadores de gestión de energía eléctrica](https://superservicios.gov.co/sites/default/files/inline-files/Indicadores-de-gestion-energia-electrica-ano-2024.pdf)
- [SSPD, multa a Enel por formación de precio en bolsa](https://www.superservicios.gov.co/Sala-de-prensa/noticias/superservicios-multa-enel-por-2847-millones-por-distorsiones-en-la-formacion-del-precio-en-bolsa-de-energia)
- [SSPD, sanción a Celsia por el apagón de Sabanalarga](https://www.superservicios.gov.co/Sala-de-prensa/noticias/superservicios-confirma-sancion-por-1700-millones-de-pesos-la-empresa-celsia-colombia-sa-esp)
- [El Colombiano, sanción a EPM por retrasos en Hidroituango](https://www.elcolombiano.com/antioquia/superintendencia-de-servicios-sanciona-a-epm-por-retrasos-en-hidroituango-NA16077138)
- [El Tiempo, sobrecostos de Hidroituango según la Contraloría](https://www.eltiempo.com/justicia/investigacion/los-sobrecostos-en-hidroituango-ya-van-en-12-2-billones-asi-va-la-construccion-de-la-megaobra-segun-reporta-la-contraloria-3543400)
- Estados financieros consolidados 2025 de ISA, EPM, Enel Colombia, Celsia e ISAGEN (SIMEV/RNVE) y Celsia, Presentación de resultados 4T 2025
