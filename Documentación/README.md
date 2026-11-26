# Documentación del proyecto

Este directorio reúne los documentos técnicos y las evidencias de aprendizaje generadas durante el desarrollo del proyecto académico de la asignatura **Diseño y Prototipado Electrónico**.

La fuente multisalida es el proyecto de aplicación. El objetivo es documentar tanto las soluciones de diseño como el proceso seguido: análisis, cálculos, selección de componentes, uso de Altium Designer, revisiones, prototipado y validación.

## Organización prevista

A medida que se generen los archivos, la documentación se organizará con la siguiente estructura:

```text
Documentación/
├── 01_Requerimientos/
│   └── Especificaciones y matriz de trazabilidad
├── 02_Arquitectura/
│   └── Diagramas de bloques y distribución de potencia
├── 03_Calculos/
│   └── Dimensionamiento eléctrico y térmico
├── 04_Componentes/
│   └── Hojas de datos, MPN y justificación de selección
├── 05_Altium/
│   └── Bibliotecas, esquemáticos y configuración del proyecto
├── 06_PCB/
│   └── Reglas de diseño, stack-up, revisión y fabricación
├── 07_Prototipo/
│   └── Ensamble, fotografías y registro de modificaciones
└── 08_Validacion/
    └── Procedimientos, mediciones y resultados de pruebas
```

Esta estructura es una guía de organización; las carpetas y documentos se incorporarán cuando exista material correspondiente. No se crearán evidencias ficticias ni se marcarán actividades como terminadas sin respaldo.

## Archivos disponibles

| Archivo | Descripción |
|:--|:--|
| [Electrical power tree](Electrical%20power%20tree.drawio) | Diagrama de distribución de potencia del sistema. |

## Criterios de documentación

Para que los archivos sean útiles durante el desarrollo y en la revisión académica:

1. **Identificar el estado del documento:** preliminar, en revisión o validado.
2. **Registrar las revisiones:** incluir fecha, cambios realizados y motivo del cambio cuando sea relevante.
3. **Conservar la trazabilidad:** relacionar los cálculos y decisiones con el requerimiento que los origina.
4. **Citar fuentes primarias:** utilizar hojas de datos oficiales del fabricante para verificar especificaciones de componentes.
5. **Separar datos y supuestos:** indicar qué valores provienen de los requisitos, cuáles de una hoja de datos y cuáles son hipótesis de cálculo.
6. **Respaldar las validaciones:** registrar instrumento, configuración, condiciones de prueba, mediciones y criterio de aceptación disponible.
7. **Documentar el aprendizaje:** conservar evidencias de configuración, bibliotecas, esquemáticos, reglas y revisiones realizadas en Altium Designer.

## Convención sugerida para archivos

Usar nombres descriptivos, sin espacios ni caracteres especiales, y añadir revisión cuando corresponda. Por ejemplo:

- `REQ_Matriz_Trazabilidad_R00.xlsx`
- `CAL_Dimensionamiento_Bus_DC_R00.pdf`
- `COMP_Registro_Componentes_R00.xlsx`
- `PCB_Revision_Distribucion_Cobre_R01.pdf`
- `TEST_Validacion_Rizado_R00.csv`

La revisión debe cambiar cuando se modifique el contenido técnico. Evitar sobrescribir resultados de pruebas anteriores; conservarlos para mantener el historial del proyecto.

## Identificación académica

- **Autor:** Henry Yesith Pabón Chapid
- **Programa:** Ingeniería Mecatrónica
- **Institución:** Universidad Tecnológica de Pereira
- **Asignatura:** Diseño y Prototipado Electrónico
- **Año:** 2026
