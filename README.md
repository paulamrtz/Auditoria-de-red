# 📊 Dashboard de Análisis de Ciberbullying
### Panel Interactivo en Power BI — Estudiantes Adolescentes

---

## 📋 Descripción del Proyecto

Panel interactivo desarrollado en **Power BI** para analizar patrones de ciberbullying en estudiantes adolescentes. Visualiza métricas clave como distribución de víctimas por género y raza, relación entre horas de pantalla y exposición al riesgo, y conductas asociadas como consumo de sustancias.

El dataset contiene información de **300 estudiantes** con variables sobre conductas de riesgo, contexto familiar, rendimiento escolar y tipos de bullying.

---

## 🛠️ Tecnologías Utilizadas

| Herramienta | Uso |
|-------------|-----|
| Power BI Desktop | Visualización y dashboard interactivo |
| DAX | Creación de medidas y métricas |
| Power Query | Limpieza y transformación de datos |
| Excel | Fuente de datos original |

---

## 📐 Medidas DAX Creadas

```dax
-- Total de estudiantes
Total_Estudiantes = COUNTROWS(variables)

-- Víctimas de ciberbullying
Ciberbullying = CALCULATE(COUNTROWS(variables), variables[Bully_Victima_Ciber] = "Si")

-- Porcentaje de víctimas
Pct_Victimas_Ciber = DIVIDE([Ciberbullying], [Total_Estudiantes]) * 100

-- Promedio de horas de pantalla
Promedio_Horas_Pantalla = AVERAGE(variables[Horas_Pantalla_Dia])

-- Víctimas de bullying físico
Bullying_Fisico = CALCULATE(COUNTROWS(variables), variables[Bully_Victima_Fisico] = "Si")

-- Víctimas de bullying verbal
Bullying_Verbal = CALCULATE(COUNTROWS(variables), variables[Bully_Victima_Verbal] = "Si")
```

---

## 📈 Hallazgos Principales

| Indicador | Resultado |
|-----------|-----------|
| Total estudiantes analizados | 300 |
| Víctimas de ciberbullying | 55 |
| Porcentaje de víctimas | 18.33% |
| Promedio de horas de pantalla/día | 4.79 hrs |
| Tipo de bullying más común | Verbal (133 víctimas) |
| Género más afectado | Femenino |
| Raza más afectada | Blanca (34.55%) |

### 🔍 Insights Clave

- 📱 **Más horas de pantalla = más riesgo** — los estudiantes con 4-5 horas diarias concentran el mayor número de víctimas
- 👩 **Las mujeres son más víctimas** de ciberbullying que los hombres
- 🗣️ **El bullying verbal es el más común** con 133 víctimas, seguido del físico (66) y el ciberbullying (55)
- 🍺 **Los agresores tienen mayor relación con el consumo de alcohol** comparado con no agresores

---

## 🖼️ Vista Previa

**Dashboard completo:**

![Dashboard](preview1.png)

---

## 📊 Visualizaciones del Dashboard

- **4 tarjetas KPI** — Total estudiantes, % víctimas, promedio hrs/pantalla, total víctimas
- **Gráfico de barras** — Víctimas por género
- **Gráfico de columnas** — Relación horas de pantalla y ciberbullying
- **Gráfico de anillos** — Distribución por raza
- **Gráfico de barras agrupadas** — Agresores y consumo de alcohol
- **Gráfico comparativo** — Tipos de bullying (Verbal, Físico, Ciber)
- **2 Slicers interactivos** — Filtro por Género y Raza

---

## 🗂️ Estructura del Proyecto

```
dashboard-ciberbullying/
├── dashboard_ciberbullying.pbix   # Archivo Power BI
├── Ciberbullying.xlsx             # Fuente de datos
├── preview1.png                   # Captura del dashboard
└── README.md                      # Documentación
```

---

## 👩‍💻 Autora

**Paula Martinez**  
Estudiante de Ingeniería en Ciencia de Datos — UNICDA  
📧 martinezpaula0728@gmail.com  
📍 Santo Domingo, República Dominicana
