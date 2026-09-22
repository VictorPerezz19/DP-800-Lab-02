# Laboratorio SQL: Implementar Objetos de Programabilidad

**Autor:** Víctor Pérez

## Entorno de Desarrollo
* **Motor de base de datos:** SQL Server 2019+ (o Azure SQL Database)
* **Cliente gráfico:** SQL Server Management Studio (SSMS)
* **Base de datos de muestra:** `AdventureWorksLT`

## Instrucciones para reproducir el trabajo

Para preparar el entorno y ejecutar los ejercicios, sigue estos pasos desde SSMS:
1. **Conexión correcta:** Conéctate a tu instancia de SQL Server y asegúrate de que la base de datos `AdventureWorksLT` esté restaurada. 
2. **Selección de base de datos:** Abre una "Nueva Consulta" (New Query) y ejecuta `USE AdventureWorksLT;` al inicio para asegurar que los scripts se apliquen en el lugar correcto.
3. **Ejecución de los scripts:** Ejecuta paso a paso los bloques de código T-SQL documentados en la práctica. Durante el proceso crearás vistas, procedimientos almacenados, funciones escalares, funciones con valores de tabla (TVF) y desencadenadores (triggers).

## Temas cubiertos
1. **Vistas (Views):** Creación de la vista `vCustomerOrders` para simplificar consultas complejas que involucran múltiples `JOIN`.
2. **Procedimientos Almacenados (Stored Procedures):** Implementación de `AddOrderLineItem` para encapsular operaciones de negocio (inserción y actualización) dentro de transacciones atómicas.
3. **Funciones Escalares (Scalar Functions):** Creación de `fnOrderTotal` para realizar cálculos matemáticos reutilizables sobre el valor total de un pedido.
4. **Funciones con Valores de Tabla en Línea (TVF):** Desarrollo de `GetCustomerOrders` para generar conjuntos de resultados parametrizados y combinarlos mediante `CROSS APPLY`.
5. **Desencadenadores (Triggers):** Configuración de `trg_LogOrderTotalChange` y la tabla `OrderAudit` para registrar y auditar automáticamente los cambios de datos (historial de precios antiguos y nuevos).

## Estructura del repositorio

De acuerdo con la estructura del proyecto, los archivos están organizados de la siguiente manera:

```text
DP-800-LAB-02/              <-- (Directorio raíz del proyecto)
├── img/                    <-- (Carpeta con las capturas de pantalla de SSMS)
├── Lab2.md                 <-- (Documentación de la práctica en formato Markdown)
├── Lab2.pdf                <-- (Documentación exportada con evidencias visuales)
└── README.md               <-- (Este archivo explicativo)
