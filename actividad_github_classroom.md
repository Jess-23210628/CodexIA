# Actividad: Propuesta de Práctica Temática Pequeña (Enfoque en Documentación)

## 1) Título de la práctica

**Diseña un título claro y concreto para tu práctica temática.**

Ejemplos de referencia:
- **Mini Toolkit en ARM64**
- **Asistente de Estudio en Terminal**
- **Reporteador de Información del Sistema**
- **Organizador de Archivos**
- **Juego de Aprendizaje en Línea de Comandos**

> Tu título debe reflejar qué problema resuelve tu práctica y para quién está pensada.

---

## 2) Descripción General

En esta actividad **vas a diseñar la propuesta de un proyecto pequeño**, priorizando la **documentación, planeación y justificación técnica** sobre la implementación extensa de código.

Debes elegir **un lenguaje principal** para tu práctica:
- **ARM64 Assembly**
- **C**
- **Python**
- **Bash**

### Reglas importantes del alcance
- El proyecto debe ser **pequeño y realizable** en tiempo corto.
- **ARM64 Assembly** se recomienda **solo para programas muy pequeños** (por ejemplo: calculadora básica, convertidor simple, lectura de argumentos y salida formateada).
- En esta fase, vale más una propuesta bien argumentada que mucho código.
- Evita: frameworks pesados, APIs pagadas, bases de datos, nube, contenedores y dependencias complejas.

### Propósito académico
Tu propuesta debe demostrar que sabes:
1. Definir un problema concreto.
2. Delimitar alcance técnico realista.
3. Organizar un repositorio de forma profesional.
4. Diseñar evidencia mínima de pruebas.

---

## 3) Entregables del Estudiante

Tu repositorio debe incluir, como mínimo:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcionales (si ya tienes avance de implementación):
- `src/`
- `scripts/`
- `tests/`

---

## 4) Estructura Recomendada del Repositorio

Usa esta estructura mínima como base:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

> `<ext>` depende del lenguaje elegido (`s`, `c`, `py`, `sh`, etc.).

---

## 5) Contenido esperado por archivo

### `README.md`
Debe incluir:
- Título del proyecto.
- Resumen de 5 a 10 líneas.
- Lenguaje principal elegido y por qué.
- Alcance del proyecto (qué sí y qué no incluye).
- Instrucciones rápidas de ejecución (aunque sea preliminar).
- Integrantes (si aplica).

### `docs/propuesta.md`
Debe incluir:
1. Problema a resolver.
2. Objetivo general y 2–3 objetivos específicos.
3. Usuario objetivo.
4. Requisitos funcionales mínimos (3 a 6).
5. Requisitos no funcionales simples (portabilidad, claridad, tamaño, etc.).
6. Justificación del lenguaje elegido.
7. Alcance y límites (qué queda fuera).

### `docs/caso_de_uso.md`
Debe incluir:
- Escenario de uso principal (paso a paso).
- Entradas esperadas del usuario.
- Salidas esperadas del programa.
- Errores comunes y manejo esperado.
- Al menos 1 caso normal y 1 caso borde.

### `docs/estructura_repositorio.md`
Debe incluir:
- Árbol del repositorio actualizado.
- Descripción breve de cada carpeta/archivo.
- Convención de nombres de archivos.
- Estrategia para separar código, scripts y pruebas.

### `docs/plan_de_pruebas.md`
Debe incluir:
- Lista de pruebas mínimas (5 o más).
- Formato sugerido por prueba:
  - ID de prueba
  - Propósito
  - Entrada
  - Resultado esperado
  - Resultado obtenido (se llena después)
  - Estatus (Pendiente / Exitosa / Fallida)

---

## 6) Restricciones Técnicas

Para asegurar que el proyecto sea viable con herramientas gratuitas:

- Mantén la solución en **modo local** (sin servicios en la nube).
- Sin bases de datos externas.
- Sin dependencias pesadas o difíciles de instalar.
- Usa bibliotecas estándar del lenguaje siempre que sea posible.
- El prototipo debe poder ejecutarse con comandos simples de terminal.

---

## 7) Sugerencias de Temas Pequeños (elige o adapta uno)

- Conversor de unidades en terminal.
- Agenda mínima de tareas en archivo de texto.
- Analizador simple de logs locales.
- Organizador de archivos por extensión.
- Quiz de comandos básicos de Linux.
- Monitor de información del sistema (CPU, memoria, disco) en formato textual.

---

## 8) Criterios de Evaluación (rúbrica sugerida)

Calificación sugerida sobre 100 puntos:

1. **Claridad de la propuesta** (20 pts)
   - Problema y objetivo bien definidos.
2. **Alcance realista** (20 pts)
   - Proyecto pequeño, factible y bien delimitado.
3. **Calidad de documentación** (30 pts)
   - Documentos completos, ordenados y comprensibles.
4. **Diseño del repositorio** (15 pts)
   - Estructura limpia y consistente.
5. **Plan de pruebas** (15 pts)
   - Casos relevantes y verificables.

---

## 9) Entrega

- Sube todos los archivos al repositorio asignado en GitHub Classroom.
- Verifica que los archivos Markdown se visualicen correctamente.
- Incluye avances de código solo si ya existen, pero recuerda: **la prioridad es la documentación**.

---

## 10) Checklist rápido antes de entregar

Marca cada punto con ✅ cuando esté listo:

- [ ] Definí un título claro y temático.
- [ ] Elegí un lenguaje principal y lo justifiqué.
- [ ] Completé `README.md`.
- [ ] Completé `docs/propuesta.md`.
- [ ] Completé `docs/caso_de_uso.md`.
- [ ] Completé `docs/estructura_repositorio.md`.
- [ ] Completé `docs/plan_de_pruebas.md`.
- [ ] Mantengo el proyecto pequeño y viable sin infraestructura compleja.

---

## Nota final del docente

La meta de esta actividad es que aprendas a **pensar y comunicar diseño técnico** antes de programar en grande. En arquitectura de computadoras y programación de sistemas, una propuesta bien delimitada evita retrabajo y mejora la calidad del desarrollo.
