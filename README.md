<!--
  Project: Multi-Output Power Supply
  Author: Henry Yesith Pabón Chapid
  Universidad Tecnológica de Pereira · Ingeniería Mecatrónica
-->

<div align="center">

  <img src="https://raw.githubusercontent.com/HenryPabon09/Project_1_Power_supply/main/assets/henry-pabon-power-supply.svg" alt="Multi-Output Power Supply — Henry Yesith Pabón Chapid" width="100%">

  <p>
    <strong>Proyecto académico de Diseño y Prototipado Electrónico.</strong>
    <br>
    Aprendizaje aplicado · Buenas prácticas de diseño · Altium Designer · Prototipado
  </p>

  <p>
    <a href="#-visión-general">Visión general</a> ·
    <a href="#-especificaciones-del-sistema">Especificaciones</a> ·
    <a href="#-arquitectura">Arquitectura</a> ·
    <a href="#-documentación">Documentación</a> ·
    <a href="#-desarrollo">Desarrollo</a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Project-In%20development-0F766E?style=flat-square" alt="Project status">
    <img src="https://img.shields.io/badge/Discipline-Power%20Electronics-2563EB?style=flat-square" alt="Discipline">
    <img src="https://img.shields.io/badge/PCB-Altium%20Designer-A855F7?style=flat-square" alt="PCB tool">
    <img src="https://img.shields.io/badge/Diagrams-diagrams.net-F59E0B?style=flat-square" alt="Diagrams tool">
  </p>
</div>

---

## ⚡ Visión general

**Multi-Output Power Supply** es un proyecto académico desarrollado en el marco de la asignatura **Diseño y Prototipado Electrónico** del programa de Ingeniería Mecatrónica de la Universidad Tecnológica de Pereira.

La fuente multisalida es el medio práctico para aplicar y fortalecer los conocimientos de diseño electrónico. El propósito no es únicamente obtener un circuito funcional: también es aprender a desarrollar un proyecto electrónico con un flujo de trabajo organizado, tomar decisiones técnicas justificadas, documentar el proceso y aplicar buenas prácticas de diseño.

Durante el desarrollo hemos profundizado especialmente en el uso de **Altium Designer**, desde la preparación del proyecto y la elaboración de esquemáticos hasta el trabajo con componentes, bibliotecas y diseño de PCB. El repositorio busca dejar evidencia de ese proceso de aprendizaje, de las decisiones tomadas y de los archivos técnicos generados.

> **Enfoque académico:** los diagramas, cálculos, esquemáticos y archivos de PCB son parte del proceso de aprendizaje y desarrollo. El estado de diseño, fabricación y validación se indicará de forma explícita para diferenciar el trabajo realizado de las pruebas que aún estén pendientes.

## 👤 Autor

**Henry Yesith Pabón Chapid**  
Estudiante de Ingeniería Mecatrónica  
Universidad Tecnológica de Pereira · Facultad de Tecnología  
Pereira, Colombia · 2026

Este repositorio documenta el trabajo realizado durante la asignatura, los conocimientos adquiridos y la aplicación de buenas prácticas de diseño y prototipado electrónico, con especial atención al flujo de trabajo en Altium Designer.

## 🔌 Especificaciones del sistema

El proyecto contempla cinco salidas DC:

| Salida | Rango / tensión nominal | Corriente máxima |
|:--|:--:|--:|
| Positiva 1 | +12 V DC | 5 A |
| Positiva 2 | +5 V DC | 5 A |
| Positiva 3 | +3.3 V DC | 3 A |
| Negativa | −12 V DC | 1 A |
| Ajustable | 1.25–15 V DC | 3 A |

Las corrientes son los límites máximos especificados para cada salida. La capacidad de operación simultánea y la potencia total disponible deberán verificarse mediante el dimensionamiento del sistema y las pruebas correspondientes.

## 🧩 Arquitectura

La arquitectura funcional definida para el proyecto sigue esta secuencia:

<div align="center">
  <img src="https://img.shields.io/badge/AC%20Input-Transformador-334155?style=for-the-badge" alt="AC input">
  <img src="https://img.shields.io/badge/Rectification-Puente%20de%20diodos-2563EB?style=for-the-badge" alt="Rectification">
  <img src="https://img.shields.io/badge/Filtering-Capacitivo-0F766E?style=for-the-badge" alt="Filtering">
  <img src="https://img.shields.io/badge/Regulation-DC%2FDC-7C3AED?style=for-the-badge" alt="DC DC">
  <img src="https://img.shields.io/badge/Outputs-5%20salidas-D97706?style=for-the-badge" alt="Outputs">
</div>

```text
Transformador AC
      │
      ▼
Puente rectificador
      │
      ▼
Filtro capacitivo
      │
      ▼
Bus DC
      │
      ├── Conversión DC/DC ── +12 V / 5 A
      ├── Conversión DC/DC ── +5 V / 5 A
      ├── Conversión DC/DC ── +3.3 V / 3 A
      ├── Conversión DC/DC ── −12 V / 1 A
      └── Conversión DC/DC ── 1.25–15 V / 3 A
```

La implementación de cada rama, sus componentes y sus condiciones de operación se documentarán conforme avance el diseño. Consulta el diagrama de distribución de potencia disponible en la sección de documentación.

## 🎓 Aprendizajes y competencias

El desarrollo de este proyecto ha permitido fortalecer conocimientos y habilidades relacionados con:

- Aplicación de buenas prácticas durante el diseño y la documentación de circuitos electrónicos.
- Manejo de Altium Designer como entorno de trabajo para el desarrollo electrónico y el diseño de PCB.
- Organización de proyectos, esquemáticos, componentes y documentación técnica.
- Interpretación de hojas de datos y consideración de parámetros eléctricos al seleccionar componentes.
- Representación de la arquitectura y distribución de potencia mediante diagramas.
- Uso de herramientas de apoyo para realizar estimaciones y comprobaciones propias del diseño de PCB.

Estos puntos representan los aprendizajes trabajados en la asignatura; los archivos y evidencias del repositorio permiten mostrar cómo se aplicaron durante el proyecto.

## 🛠️ Herramientas de desarrollo

| Herramienta | Aplicación |
|:--|:--|
| **Altium Designer** | Captura esquemática, bibliotecas y diseño de PCB |
| **diagrams.net** | Diagramas de bloques y arquitectura eléctrica |
| **Saturn PCB Toolkit** | Estimaciones de pistas, corriente, caída de tensión y vías |
| **DigiKey / LCSC** | Consulta y verificación de componentes comerciales |
| **Datasheets oficiales** | Verificación de límites y características eléctricas |

## 🧩 Estado actual del diseño

Ya se dispone de esquemáticos de la etapa DC-DC y de vistas 2D y 3D de la PCB elaboradas en Altium Designer. En el esquemático se distinguen cinco ramas de conversión desde 24 V; las vistas de PCB permiten revisar la distribución de componentes y las notas preliminares de fabricación.

Este avance corresponde al diseño en CAD. No debe interpretarse como evidencia de fabricación ni de validación eléctrica, térmica o funcional. El detalle de lo observado y las verificaciones pendientes se encuentra en [Estado actual del diseño](Documentaci%C3%B3n/Estado_actual_del_diseno.md).

## 📁 Documentación

| Recurso | Descripción |
|:--|:--|
| [Electrical power tree](Documentaci%C3%B3n/Electrical%20power%20tree.drawio) | Diagrama de distribución y ramas de potencia |
| [Índice de documentación](Documentaci%C3%B3n/README.md) | Estructura, criterios y convenciones para organizar los documentos técnicos y evidencias de aprendizaje |\n| [Estado actual del diseño](Documentaci%C3%B3n/Estado_actual_del_diseno.md) | Registro del esquemático DC-DC y las vistas 2D/3D de PCB, con verificaciones pendientes |
| Datasheets de componentes | Se incorporarán con sus MPN exactos, revisión y enlace oficial del fabricante una vez verificados y organizados en el repositorio |

La documentación se organizará por etapas: requerimientos, arquitectura, cálculos, componentes, desarrollo en Altium, PCB, prototipado y validación. Consulta el [índice de documentación](Documentaci%C3%B3n/README.md) para conocer la estructura prevista y los criterios de registro. Los enlaces a hojas de datos y componentes comerciales deben apuntar a documentos oficiales y referencias exactas.

## 🧪 Desarrollo

El proyecto se desarrolla como un proceso académico y práctico. Las actividades principales incluyen:

- [ ] Consolidación y trazabilidad de requerimientos.
- [ ] Definición y revisión de la arquitectura eléctrica.
- [ ] Dimensionamiento de rectificación y filtrado.
- [ ] Selección y verificación de convertidores y componentes de potencia.
- [ ] Desarrollo y revisión de esquemáticos.
- [ ] Diseño de PCB y revisión de reglas eléctricas.
- [ ] Fabricación y ensamblaje del prototipo.
- [ ] Validación eléctrica, térmica y funcional.
- [ ] Documentación de resultados y mejoras.

El estado de cada actividad se actualizará con evidencia técnica; no se marcará como completada únicamente por disponer de un archivo de diseño.

## 📐 Criterios de ingeniería

Durante el desarrollo se prestará especial atención a:

- Márgenes de tensión y corriente de los componentes.
- Pérdidas de conversión y eficiencia por rama.
- Rizado, respuesta transitoria y regulación.
- Disipación térmica y temperatura de operación.
- Ancho de pistas, caída de tensión y distribución de retornos.
- Protección frente a cortocircuito, sobrecorriente y sobretemperatura.
- Accesibilidad para medición, inspección y mantenimiento.

Los valores finales, tolerancias y criterios de aceptación se documentarán con su fuente y método de verificación.

## 📌 Estado del proyecto

**Proyecto académico en desarrollo.** El repositorio se actualizará progresivamente con los avances de diseño, ejercicios de aplicación, decisiones técnicas, archivos de Altium, documentación de componentes y evidencias de prototipado y validación.

---

<div align="center">

  **Diseñado y documentado por Henry Yesith Pabón Chapid**

  *Power electronics · Embedded hardware · PCB design*

  <sub>Universidad Tecnológica de Pereira · 2026</sub>

</div>
