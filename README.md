
#  ConnectaTel – Análisis de Uso de Clientes

##  Objetivo del Proyecto

Este proyecto tiene como objetivo analizar el comportamiento real de los clientes de ConnectaTel (México y Colombia) en el uso de servicios móviles (llamadas y mensajes).

A través de este análisis se busca:

- Identificar patrones de uso de los clientes
- Detectar valores atípicos (outliers) y posibles anomalías
- Comprender cómo varía el uso según edad y tipo de plan
- Generar insights accionables para optimizar la oferta comercial y mejorar la experiencia del usuario

---

##  Datasets Utilizados

Se trabajó con tres fuentes de datos:

### 1. `plans.csv`
Contiene información sobre los planes disponibles:
- Precio
- Minutos incluidos
- GB incluidos
- Costos por consumo extra

### 2. `users_latam.csv`
Información de clientes:
- Edad
- Ciudad
- Fecha de registro
- Plan contratado

### 3. `usage.csv`
Detalle de uso de los usuarios:
- Llamadas (duración)
- Mensajes (cantidad/longitud)

---

##  Etapas del Análisis

El proyecto se desarrolló siguiendo un flujo estructurado:

### 1. Carga y exploración de datos
- Inspección de estructuras, tipos de datos y consistencia

### 2. Identificación de problemas de calidad
- Valores nulos
- Valores inválidos (ej. `-999`, `"?"`)
- Fechas fuera de rango

### 3. Limpieza de datos
- Reemplazo de valores inválidos por nulos
- Conversión de tipos de datos
- Validación de fechas

### 4. Análisis descriptivo
- Cálculo de métricas clave:
  - Media
  - Mediana
  - Percentiles

### 5. Visualización y detección de outliers
- Histogramas
- Boxplots
- Identificación de distribución y valores extremos

### 6. Segmentación de usuarios
- Por edad:
  - Jóvenes
  - Adultos
  - Adultos mayores
- Por nivel de uso:
  - Bajo
  - Medio
  - Alto

### 7. Generación de insights
- Identificación de patrones de consumo
- Detección de usuarios intensivos (cola larga)
- Relación entre uso y tipo de plan

---

## Principales Hallazgos

- Existe una **distribución de cola larga**, donde pocos usuarios concentran gran parte del consumo.
- Los usuarios de **uso medio** representan la mayoría de la base.
- Los usuarios de **alto uso** son clave para ingresos, pero también implican mayores costos.
- Los **jóvenes** tienden a mayor uso (especialmente en mensajería).
- Los **adultos** presentan comportamiento más equilibrado.

---

## Recomendaciones

- Diseñar estrategias para migrar usuarios de uso medio a planes Premium
- Implementar acciones de retención para usuarios de alto valor
- Crear incentivos para aumentar el engagement de usuarios de bajo uso
- Mejorar controles de calidad de datos en origen

Guía de Reproducción

Para reproducir el análisis:

Asegurarse de contar con los 3 datasets en la misma carpeta

- Ejecutar el notebook desde el inicio

- Seguir el flujo:

    Limpieza de datos

    Análisis exploratorio

    Visualización

    Segmentación

    Revisar las conclusiones al final del notebook
  
-  Herramientas Utilizadas

    Python

    Pandas

    NumPy

    Matplotlib
    
    Seaborn

    Jupyter Notebook
