# CDSS Medicina Interna | Suite de Análisis Fisiopatológico

![Version](https://img.shields.io/badge/version-3.0_R4_Edition-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Privacy](https://img.shields.io/badge/privacy-client--side-secure)

Herramienta de Soporte a la Decisión Clínica (**CDSS**) desarrollada para residentes y especialistas en Medicina Interna. Este software ejecuta un análisis de texto sobre notas de evolución médica (formato libre) para extraer biomarcadores y calcular índices fisiopatológicos complejos en tiempo real.

## 📋 Características Clínicas

El algoritmo procesa variables bioquímicas y hematológicas basándose en las guías de práctica clínica más recientes:

### 🩸 Hematología Avanzada
- **Clasificación Dinámica de Anemias:** Cruce de variables VCM/HCM con RDW para diagnósticos diferenciales (Ferropenia vs Talasemia vs Enfermedad Crónica).
- **Índice Reticulocitario:** Diferenciación entre anemia regenerativa (hemólisis/sangrado) vs arregerativa.
- **Alertas de Series:** Detección de trombocitopenia crítica y poliglobulia.

### 🧬 Nefrología (KDIGO 2024)
- **Cálculo de TFGe:** Ecuación **CKD-EPI 2021** (sin variable de raza) ajustada por sexo y edad.
- **Estadificación:** Clasificación automática G1-G5.
- **Fenotipo de Falla Renal:** Cálculo de relación BUN/Creatinina para sugerir etiología Prerrenal vs NTA.

### ⚡ Medio Interno y Electrolitos
- **Osmolaridad:** Cálculo de Osmolaridad efectiva y detección de GAP Osmolar (tóxicos/alcoholes).
- **Disnatremias:** Corrección automática de Sodio por hiperglucemia (Factor de Katz).
- **Metabolismo Mineral:** Calcio corregido por albúmina.

### 🧪 Hepatología
- **Índice de De Ritis:** Relación AST/ALT para orientación etiológica (Alcohólica vs Viral/NAFLD).
- **Función Sintética:** Evaluación de albumina y tiempos.

## 🔒 Privacidad y Seguridad (Client-Side)

Esta herramienta sigue una arquitectura **Zero-Knowledge**:
1. **Procesamiento Local:** Todo el código se ejecuta exclusivamente en el navegador del usuario.
2. **Sin Base de Datos:** No se envían datos a ningún servidor externo.
3. **Persistencia Nula:** Al cerrar la pestaña, los datos del paciente se eliminan permanentemente de la memoria RAM.

## 🚀 Uso

1. Copie su nota de evolución médica (o digite los laboratorios en bruto).
2. Pegue el texto en el área de análisis.
3. El sistema reconocerá patrones mediante **Expresiones Regulares (RegEx)** como `Hb 10`, `Na 135`, `Cr 1.2`.

## ⚠️ Aviso Legal (Disclaimer)

**Este software es una herramienta educativa y de apoyo.**
Los algoritmos presentados son auxiliares y **NO sustituyen el juicio clínico profesional**. El autor no se hace responsable por decisiones tomadas basándose únicamente en este software. El médico tratante es el único responsable del diagnóstico y manejo del paciente.

---
**Desarrollado por:** Dr. Andy Torreblanca González
*Residente de Medicina Interna (R4)*
