# Trabajo 02: Decisión Multicriterio (trabajo02indtd2025)

**Autor:** Francisco Javier López León
**Asignatura:** Teoría de la Decisión

---

## 📄 Ver el Informe Final

El informe completo, con toda la metodología, análisis, tablas y gráficos, está disponible en formato HTML.

> **[Haz clic aquí para ver el informe renderizado (Trabajo2.html)](https://htmlpreview.github.io/?https://github.com/fralopleo2/trabajo02indtd2025/blob/main/Trabajo2.html)**

---

## 1. Descripción del Problema

Este repositorio contiene la resolución del Trabajo 02. El objetivo es aplicar diversas técnicas de decisión multicriterio (MCDM) para resolver el problema de la **"Selección del mejor piso de alquiler para un estudiante"**.

Se evalúan 4 alternativas de pisos:
* **A_Cercano**: Al lado de la facultad, pero caro y antiguo.
* **B_Reformado**: Algo alejado, pero moderno, de alta calidad y precio medio.
* **C_Barato**: Muy lejos y de baja calidad, pero extremadamente barato.
* **D_Centrico**: En el centro, ideal para ocio, pero ruidoso y lejos de la facultad.

La evaluación se basa en 10 subcriterios, agrupados en 4 criterios principales:
1.  **Económico** (Alquiler, Gastos, Transporte)
2.  **Ubicación** (Tiempo Uni, Conexión, Servicios)
3.  **Calidad** (Estado, Tamaño Hab.)
4.  **Ambiente** (Ruido, N.º Compis)

## 2. Métodos Aplicados

El análisis se realiza en el fichero `Trabajo2.qmd` y aplica las tres técnicas vistas en clase, cumpliendo con los requisitos de la evaluación:

1.  **AHP (Analytic Hierarchy Process) con Paquete:**
    * Se utiliza el paquete `ahp` de R.
    * La jerarquía completa y las comparaciones 2 a 2 están definidas en el fichero `pisos.ahp` (usando la sintaxis de la Versión 2.0).
    * Se analizan los rankings y la consistencia de todas las matrices.

2.  **AHP con Funciones R:**
    * Se replica el análisis anterior usando las funciones (`*.R`) proporcionadas por la asignatura.
    * Se valida la consistencia de las 14 matrices (CI < 0.10) y se comprueba que el ranking es idéntico al obtenido con el paquete.

3.  **ELECTRE I:**
    * Se utiliza un método de superación no compensatorio.
    * Se definen umbrales de veto para los criterios más importantes (Alquiler y Tiempo Uni).
    * Se realiza el análisis iterativo para encontrar el núcleo.

4.  **PROMETHEE II:**
    * Se utiliza un método de flujos netos para obtener un ranking completo.
    * Se definen funciones de preferencia (Usual, V-shape, Linear) para los 10 subcriterios.

## 3. Archivos del Repositorio

* `Trabajo2.qmd`: **(Archivo Fuente)** Fichero principal de Quarto (R) con todo el código, los análisis y las conclusiones.
* `Trabajo2.html`: **(Informe Final)** Salida HTML renderizada del trabajo.
* `pisos.ahp`: Documento YAML (v2.0) que define la jerarquía y las matrices de comparación para el paquete `ahp`.
* `teoriadecision_*.R`: Los 3 archivos de funciones R proporcionados por el profesor para AHP-R, ELECTRE y PROMETHEE.
* `diagrama.png`: (Si lo has subido) Imagen estática del diagrama AHP para el PDF.
