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
