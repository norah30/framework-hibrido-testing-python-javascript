# Framework Híbrido de Testing con Python y JavaScript

Framework de pruebas que combina técnicas avanzadas de testing en **Python** (pytest, Hypothesis, mutmut) y **JavaScript** (Jasmine), aplicadas sobre una calculadora con historial y cálculo de impuestos. Incluye pruebas basadas en propiedades, mutation testing, contract testing, pruebas combinatorias y análisis de confiabilidad.

---

## Descripción general

Este proyecto implementa un mini-framework híbrido que extiende las capacidades de Jasmine y pytest, proporcionando:

- **Pruebas de integración** con gestión de contexto y dependencias
- **Mocking avanzado** con espías personalizados (Jasmine Spies)
- **Generación de pruebas basada en tipos** con validación automática
- **Property-based testing** con Hypothesis (Python)
- **Mutation testing** con mutmut (score objetivo: >78%)

---

## Componentes del proyecto

### Módulo JavaScript — ServicioCalculadora

Calculadora con operaciones básicas (sumar, restar, multiplicar, dividir), cálculo de impuestos mediante servicio externo y registro completo de historial de operaciones. Implementa **inyección de dependencias** para facilitar mocks y espías en Jasmine.

### Módulo Python — Búsqueda Binaria

Implementación iterativa y recursiva del algoritmo de búsqueda binaria con análisis de complejidad ciclomática (Radon) y pruebas de mutación.


## Estructura del proyecto

```
framework-hibrido-testing-python-javascript/
├── src/
│   ├── js/servicios/         # ServicioCalculadora (JavaScript)
│   └── python/               # Búsqueda binaria (Python)
├── spec/                     # Pruebas Jasmine (JavaScript)
├── tests/                    # Pruebas pytest (Python)
├── .hypothesis/              # Configuración property-based testing
├── mutants/                  # Resultados mutation testing
├── cobertura/                # Reportes de cobertura
├── analisis_estatico/        # Análisis complejidad ciclomática
├── makefile                  # Automatización de tareas
└── package.json              # Dependencias JavaScript
```

---

## Instalación

```bash
# Clonar el repositorio
git clone https://github.com/norah30/framework-hibrido-testing-python-javascript.git
cd framework-hibrido-testing-python-javascript

# Dependencias JavaScript
npm install

# Dependencias Python
pip install pytest pytest-cov hypothesis mutmut allpairspy pylint radon numpy pandas matplotlib scikit-learn
```

---

## Uso

```bash
# Pruebas JavaScript (Jasmine)
npm test

# Pruebas Python con cobertura
pytest --cov=src/python

# Mutation testing
mutmut run
mutmut results

# Análisis estático
pylint src/python/
```

---

## Resultados de calidad

| Técnica | Resultado |
|---|---|
| Cobertura pytest | 92% |
| Mutation score (mutmut) | 78.9% (30 killed / 8 survived) |
| Casos Pairwise generados | 15 de 60 posibles |

---

## Tecnologías

**Python:** pytest, pytest-cov, Hypothesis, mutmut, allpairspy, Radon, NumPy, Pandas, Matplotlib, scikit-learn

**JavaScript:** Jasmine, Node.js
