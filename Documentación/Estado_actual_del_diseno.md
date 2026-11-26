# Estado actual del diseño

**Estado documental:** avance de diseño en Altium Designer.  
**Evidencia:** capturas de pantalla compartidas del proyecto `Project1_Power_Supply.PrjPcb` en Altium Designer 25.8.1 (Trial).  
**Alcance de esta revisión:** interpretación visual de los esquemáticos y de las vistas 2D/3D de la PCB. No equivale a una auditoría del proyecto fuente ni a una validación eléctrica.

## 1. Esquemático de la etapa DC-DC

En la captura del documento `200_DC-DC.SchDoc` se observan cinco ramas de conversión con entrada rotulada como 24 V:

| Rama | Salida indicada en el esquemático | Observación |
|:--|:--:|:--|
| DC/DC 1 | +12 V DC | Se identifica el bloque de conversión y su red de realimentación. |
| DC/DC 2 | +5 V DC | Se identifica el bloque de conversión y su red de realimentación. |
| DC/DC 3 | +3.3 V DC | Se identifica el bloque de conversión y su red de realimentación. |
| DC/DC 4 | −12 V DC | Se identifica una etapa dedicada a la salida negativa. |
| DC/DC 5 | 1.25–15 V DC | Salida ajustable; el esquema muestra un controlador LM76003. |

La captura permite reconocer la organización de las ramas y algunos componentes/controladores. Para verificar valores, conexiones, tolerancias, márgenes y cumplimiento de requisitos es necesario revisar los archivos esquemáticos originales y las hojas de datos correspondientes.

## 2. Vista 2D de la PCB

La vista 2D de `Main_PCB_V1R0_DDMMYY.PcbDoc` muestra una tarjeta con componentes distribuidos sobre la placa, zonas de cobre y conectores asociados a las salidas.

En las notas de fabricación visibles en la captura se indican los siguientes parámetros:

| Parámetro | Valor indicado |
|:--|:--|
| Material dieléctrico | FR-4 |
| Espesor | 1.6 mm |
| Máscara antisoldante | Negra |
| Serigrafía | Blanca |
| Cobre | 1 oz |
| Acabado superficial | Pb-Free HASL |
| Número de capas | 2 |

Estos son los valores que aparecen en la nota de fabricación de la captura. Deben contrastarse con la configuración real de fabricación y con los archivos de salida antes de enviar la placa a producir.

## 3. Vista 3D de la PCB

La vista 3D permite inspeccionar visualmente la ubicación y orientación de componentes, conectores, elementos mecánicos y la distribución general de la tarjeta. Es útil para detectar posibles problemas de montaje, accesibilidad y coherencia entre encapsulados y componentes previstos.

La vista 3D, por sí sola, no demuestra que las huellas sean correctas, que las conexiones eléctricas estén completas ni que el diseño cumpla los requisitos térmicos o de corriente.

## 4. Estado y verificaciones pendientes

| Área | Evidencia disponible | Estado de validación |
|:--|:--|:--|
| Esquemático DC-DC | Captura del esquemático en Altium | Revisión visual preliminar; falta auditoría de conexiones y cálculos. |
| Distribución PCB 2D | Captura del documento PCB | Diseño visual disponible; falta revisar reglas y resultados DRC. |
| Ensamble 3D | Captura de la vista 3D | Inspección visual preliminar; falta verificación física de componentes y alturas. |
| Fabricación | Notas de fabricación visibles en PCB | Parámetros indicados; no constituyen evidencia de fabricación. |
| Pruebas eléctricas | No se aportaron mediciones en estas capturas | Pendientes de documentar. |
| Pruebas térmicas y funcionales | No se aportaron resultados en estas capturas | Pendientes de documentar. |

### Próximas revisiones técnicas recomendadas

1. Revisar los esquemáticos completos y ejecutar las comprobaciones eléctricas/ERC disponibles.
2. Confirmar la correspondencia entre cada salida, su conector, su plano de retorno y su protección.
3. Revisar reglas de diseño PCB (DRC), anchos de pista, vías, separación, clearance y capacidad de corriente.
4. Verificar el stack-up, espesor de cobre y especificaciones con el fabricante seleccionado.
5. Comprobar footprints, pinout, dimensiones mecánicas y alturas de los componentes.
6. Revisar disipación térmica, lazos de corriente de conmutación, desacoplo y rutas de retorno.
7. Documentar las pruebas del prototipo con instrumentos, condiciones, mediciones y criterios de aceptación.

> **Nota:** las capturas compartidas se utilizaron como evidencia visual para esta descripción. Los archivos de imagen originales todavía no están incorporados como adjuntos dentro de este repositorio. Cuando se añadan a `assets/evidence/`, se podrán enlazar aquí para consulta directa.

---
*Documento de seguimiento académico. Actualizar esta página cuando existan nuevas revisiones del esquemático, PCB, fabricación o pruebas.*
