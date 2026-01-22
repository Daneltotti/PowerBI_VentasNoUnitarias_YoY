# Análisis de Ventas No Unitarias – Comparativa 2024 vs 2025

Este proyecto analiza la evolución de las ventas no unitarias (ventas con más de una unidad por transacción) en distintos países, comparando los años 2024 y 2025. El objetivo es identificar tendencias, variaciones interanuales y comportamientos atípicos por país.

---

## 🎯 Objetivos del análisis

1. Determinar si la proporción global de ventas no unitarias aumentó o disminuyó entre 2024 y 2025.
2. Identificar el país con mayor proporción de ventas no unitarias.
3. Detectar qué país tuvo la mayor caída interanual en su % de ventas no unitarias.

---

## 🧮 Métrica principal (% VNU)

Se creó una medida DAX personalizada para calcular el porcentaje de ventas no unitarias:

```DAX
% VNU = 
    VAR CantidadVentasMayor1 = 
        CALCULATE(COUNTROWS(Ventas), Ventas[Cantidad] > 1)
    VAR CantidadVentas =
        COUNTROWS(Ventas)
    RETURN DIVIDE(CantidadVentasMayor1, CantidadVentas)
Además, se utilizó la medida rápida de Power BI para calcular la variación interanual (YoY).

---

## 📊 Visualizaciones incluidas

- Tabla comparativa por país con:
  - % VNU 2024  
  - % VNU 2025  
  - Variación interanual YoY  
- Segmentadores por país y año  
- Vista general del comportamiento regional  

---

## 📁 Archivos incluidos

- **VentasNoUnitarias_YoY_2024_2025.pbix** → Archivo principal del proyecto  
- **capturas/** → Carpeta con imágenes del informe  

---

## 📸 Captura del informe

![Tabla comparativa % VNU](capturas/tabla_vnu_yoy.png)

---

## 🧠 Resultados principales

- La proporción global de ventas no unitarias **disminuyó** entre 2024 y 2025.  
- El país con mayor proporción de ventas no unitarias fue **Ecuador**, con un YoY del **0%**.  
- El país con mayor caída interanual fue **Colombia**, con un YoY de **-80%**.  

---

## 🧠 Reflexión personal

Este proyecto me permitió aplicar lógica de negocio con DAX, interpretar variaciones interanuales y construir visualizaciones comparativas. Refuerza mi experiencia en análisis de datos aplicados y mi capacidad para comunicar resultados de forma clara.

---

## 📌 Autor

**Arian Danel Bertotto**  
Junior Data Analyst – Python | SQL | Power BI
