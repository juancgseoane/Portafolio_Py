# 📊 Proyectos de Análisis de Datos con Python y SQL

Este repositorio contiene distintos proyectos de **análisis de datos** realizados con **Python, SQL y PostgreSQL**, aplicando técnicas de limpieza, transformación y generación de reportes útiles para la toma de decisiones en entornos empresariales.  

---

## 🚀 Tecnologías utilizadas
- **Python 3.10+**
- **PostgreSQL**
- **SQLAlchemy / psycopg2**
- **pandas / numpy**
- **Jupyter Notebook**

---

## ⚙️ Flujo de trabajo aplicado

1. **Conexión a bases de datos**  
   Uso de **SQLAlchemy** y **psycopg2** para conectarse a PostgreSQL y extraer datos en formato tabular.

2. **Carga de tablas en DataFrames**  
   Implementación de funciones reutilizables (`leer_tabla`) para importar tablas completas a pandas.

3. **Integración y validación de datos**  
   - Cruce de DataFrames (`merge`) asegurando integridad referencial con `validate`.  
   - Identificación de relaciones **1:m** y **m:1** entre entidades.

4. **Cálculo de métricas**  
   Generación de nuevas columnas como:
   - **venta** = `quantityOrdered * priceEach`  
   - **costo** = `quantityOrdered * buyPrice`  
   - **ganancia** = `venta - costo`

5. **Análisis y reportes**  
   - Ventas por línea de producto.  
   - Clientes con y sin compras.  
   - Top 10 de clientes y productos por periodo.  
   - Reportes pivotados para análisis dinámico.  

6. **Funciones genéricas (principio DRY)**  
   Centralizadas en un módulo `funciones.py`:  
   - `filtrar_por_fechas()` → filtra DataFrames por rangos de fechas.  
   - `generar_reporte()` → genera reportes dinámicos tipo tabla pivote.  
   - `escribir_en_base_de_datos()` → guarda DataFrames en PostgreSQL.  

---

