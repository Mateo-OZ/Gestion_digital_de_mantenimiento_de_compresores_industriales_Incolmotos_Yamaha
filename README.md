# Gestión digital de mantenimiento de compresores industriales – Incolmotos Yamaha

## Descripción del proyecto

Este repositorio contiene la documentación, estructura de datos, scripts SQL y entregables de una solución orientada a la **gestión digital del mantenimiento de compresores industriales** en el contexto de **Incolmotos Yamaha**.

El proyecto abarca desde el modelado de datos y la creación de la base de datos relacional, hasta el diseño de una aplicación web para el registro de intervenciones y la definición de indicadores clave para un dashboard analítico. El desarrollo se organiza por sprints bajo metodología Scrum.

## Objetivo

Mejorar la trazabilidad y capacidad de análisis del mantenimiento de los compresores industriales, a través de una base estructurada que permita administrar la información relacionada con:

- Equipos industriales
- Técnicos responsables
- Tipos de novedad o falla
- Componentes y repuestos
- Intervenciones de mantenimiento
- Relación entre intervenciones y técnicos
- Detalle de repuestos/componentes usados en cada intervención

## Alcance funcional

La solución permite:

- Registrar equipos y sus características
- Registrar técnicos y su entidad
- Clasificar tipos de novedad
- Gestionar repuestos y componentes
- Registrar intervenciones de mantenimiento
- Asociar uno o varios técnicos a una intervención
- Registrar detalle de componentes y repuestos utilizados
- Ejecutar consultas de validación, conteo y análisis de datos
- Capturar información mediante formularios web
- Definir indicadores clave de mantenimiento para análisis posterior

## Tecnologías

| Componente | Tecnología |
|---|---|
| Base de datos | PostgreSQL |
| Modelado | Esquema en estrella |
| Scripts | SQL (DDL, DML, consultas analíticas) |
| Aplicación web | Desplegada en Vercel |
| Datos de carga | CSV / Excel |
| Documentación | PDF |

## Equipo

| Integrante | Rol |
|---|---|
| David Salcedo Higuita | Product Owner |
| Juan Manuel Arias Gutiérrez | Analista Ax |
| Mateo Ortiz Zapata | Desarrollador Backend |
| Simón Sánchez Gómez | Analista BI/Modelo |
| Yoshuan David Pabón Mejía | Scrum Master |

## Estructura del repositorio

```text
Gestion_digital_de_mantenimiento_de_compresores_industriales_Incolmotos_Yamaha/
│
├── README.md
├── diagrama.png
├── modelo estrella.png
├── Criterios de inclusión y estructura mínima estandarizada de los registros.pdf
├── Diccionario_De_Datos.pdf
├── Informe sobre vacíos de información e inconsistencias.pdf
│
├── Sprint 2/
│   ├── Datos tablas/
│   │   ├── Componentes.csv
│   │   ├── Detalle_intervencion.csv
│   │   ├── Equipos.csv
│   │   ├── Intervencion_tecnico (2).csv
│   │   ├── Intervenciones (2).csv
│   │   ├── Repuestos.csv
│   │   ├── Tecnicos (2).csv
│   │   └── Tipo_novedad.csv
│   ├── Consultas.sql
│   ├── creacion_esquema_base_de_datos.sql
│   ├── privilegios_usuarios.sql
│   ├── Datos.xlsx
│   ├── Criterios de inclusión y estructura mínima estandarizada de los registros (1).pdf
│   ├── Diccionario_De_Datos_Actualizado.pdf
│   ├── Informe sobre validez del esquema en estrella.pdf
│   └── modelo entidad-relacion.png.png
│
└── Sprint 3/
    ├── 03_Definicion_resultados_a_medir.pdf
    ├── 05_Definicion_datos_dashboard.pdf
    ├── Documentación formulario.pdf
    ├── Estructura_Interfaz-1.pdf
    ├── HU12_interfaz.pdf
    └── HU15_Indicadores_Mateo.pdf
```

## Avance por sprints

### Sprint 1 – Levantamiento de información
- Diccionario de datos inicial.
- Criterios de inclusión y estructura mínima estandarizada de los registros.
- Informe sobre vacíos de información e inconsistencias.
- Diagramas del modelo (relacional y estrella).

### Sprint 2 – Implementación de la base de datos
- Esquema SQL con creación de 8 tablas (DDL).
- Roles y permisos de base de datos.
- Datos de carga en CSV y Excel.
- Consultas de validación, conteo y análisis.
- Diccionario de datos actualizado.
- Informe de validez del esquema en estrella.

### Sprint 3 – Diseño de la aplicación web y definición analítica
- Aplicación web funcional desplegada en Vercel para registro y consulta de intervenciones.
- Documento de diseño de la estructura de la interfaz del sistema.
- Documento de diseño de formularios de ingreso de datos.
- Documento de definición de resultados que se quieren medir.
- Selección y definición de 5 indicadores clave alineados con el objetivo del proyecto:
  - Reincidencia de fallas por tipo de falla.
  - Tiempo promedio de mantenimiento.
  - Piezas que más fallan por máquina.
  - Repuestos más utilizados por máquina.
  - Frecuencia de mantenimientos por compresor.
- Documento de definición de datos a mostrar en el dashboard.

## OKR del proyecto

| Key Result | Descripción | Estado |
|---|---|---|
| KR1 | Estructurar el 100% de los registros históricos en una base consolidada y consultable. | Finalizado |
| KR2 | Contar con al menos 5 indicadores implementados. | En progreso |
| KR3 | Identificar al menos 3 patrones recurrentes de falla. | No iniciado |
| KR4 | Lograr que el modelo descriptivo permita comparar fallas por criticidad en el 100% de los casos. | No iniciado |

## Próximos pasos (Sprint 4)

- Implementar un dashboard inicial con los indicadores que puedan medirse con la información disponible.
- Validar cada indicador frente al objetivo del proyecto.
- Definir la clasificación de fallas por criticidad como base para el KR4.
- Iniciar el análisis de patrones recurrentes de falla.
- Realizar pruebas funcionales de la aplicación antes de integrar la capa analítica.
