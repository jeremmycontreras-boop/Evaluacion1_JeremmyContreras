# Evaluacion1_JeremmyContreras
Este repositorio contiene el desarrollo correspondiente al informe técnico sobre el análisis de deflexión teórica versus medida en una viga simplemente apoyada con carga puntual centrada, aplicando la teoría de flexión de Euler-Bernoulli.

El proyecto está organizado con la siguiente estructura de archivos:

```text
README.md
data/datos_viga.csv               # Registro de cargas (P) y deflexiones medidas
data/parametros_viga.xlsx         # Geometría de la sección (L, b, h) y módulo elástico (E)
analysis/analisis_viga.xlsx       # Planilla con datos y cálculos numéricos
figures/carga_deflexion.png       # Gráfico comparativo Carga vs. Deflexión
figures/esquema_viga.png          # Diagrama conceptual de la viga      
report/main_sections.tex          # Contenido técnico y secciones del informe
report/bibfile.bib                # Base de datos bibliográfica (BibTeX)
report/nota_tecnica.pdf           # Informe final compilado
USO_IA.md                         # Declaración formal sobre el uso de IA

1. Archivos Base y Procesamiento de Datos:
   - "parametros_viga.xlsx": Lectura e interpretación de las propiedades geométricas y mecánicas del elemento (L = 4 [m] , b = 0.2 [m], h = 0.4 [m] y E = 25 [GPa]).
   - "datos_viga.csv": Procesamiento de la serie de datos de carga puntual P (0 a 40 [kN]) y sus correspondientes deflexiones medidas (0 a 2.05 [mm]).
   - "analisis_viga.xlsx": Elaboración de la planilla consolidada con fórmulas automatizadas para la conversión de unidades, cálculo de deflexión teórica (delta_teo) y determinación de porcentajes de error relativo.

2. Cálculos y Conversión de Unidades:
   - Determinación del segundo momento de área (I) para la sección rectangular (b = 0.2 [m], h = 0.4 [m]):
     I = b h^3 / 12 = 0.0010667 [m^4]
   - Conversión de magnitudes al Sistema Internacional (kN a N, GPa a Pa, m a mm).
   - Verificación analítica de la rigidez equivalente del sistema (k_teo = 20.0 [kN/mm]).

3. Análisis e Interpretación de Resultados:
   - Comparación directa entre la deflexión medida en ensayo (delta_med) y la calculada mediante la teoría de Euler-Bernoulli (delta_teo).
   - Evaluación del porcentaje de error relativo, obteniendo un valor máximo de solo 2.67% para P = 30 [kN], confirmando la validez del modelo elástico lineal.

4. Documentación Técnica en LaTeX:
   - Compilación de la nota técnica en Overleaf ajustada a la pauta de 2 a 3 páginas.
   - Formato continuo con abstract/resumen, metodología, tabla de resultados, gráfico comparativo, limitaciones del modelo y bibliografía en formato BibTeX.
