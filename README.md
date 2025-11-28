# Proyecto Final: Topología Computacional y Análisis Topológico de Datos (TDA)

Este repositorio contiene la implementación en Python de una librería para el análisis y cálculo de homología simplicial, desarrollada como parte de la asignatura de Topología Computacional.

## Funcionalidades Implementadas

El proyecto se estructura en una clase principal 'SimplicialComplex' que permite modelar objetos topológicos y calcular sus invariantes algebraicos.

### 1. Estructuras y Topología Básica
- **Gestión de Complejos:** Inserción de símplices y clausura automática de caras.
- **Operaciones Topológicas:** Cálculo de la *Estrella* (Star) y el *Link* de un símplice.
- **Conectividad:** Cálculo de componentes conexas ($\beta_0$) mediante estructuras de conjuntos disjuntos (Union-Find).
- **Característica de Euler:** Cálculo del invariante topológico $\chi = \sum (-1)^k s_k$.

### 2. Álgebra Homológica
- **Cálculo de Homología:** Implementación de la **Forma Normal de Smith** sobre $\mathbb{Z}_2$ para calcular el rango de matrices de borde.
- **Números de Betti:** Algoritmo general para obtener $\beta_p$ (número de agujeros $p$-dimensionales) a partir de las matrices borde.

### 3. Filtraciones y Complejos Geométricos
- **Complejo de Vietoris-Rips:** Construcción eficiente del complejo a partir de nubes de puntos en $\mathbb{R}^n$, calculando distancias y cliques.
- **Algoritmo Incremental:** Cálculo paso a paso de los cambios en la homología (nacimiento y muerte de ciclos) conforme se añaden símplices a la filtración.
- **Alfa Complejos:** Integración con la librería 'Gudhi' para el cálculo preciso de complejos basados en diagramas de Voronoi y Delaunay.

## Requisitos Técnicos

Este proyecto utiliza las siguientes librerías para el cálculo numérico y geométrico:

- 'numpy': Operaciones matriciales y álgebra lineal.
- 'scipy': Cálculos espaciales (Voronoi).
- 'matplotlib': Visualización de complejos simpliciales 2D.
- 'gudhi': (Opcional) Para la generación optimizada de Alfa Complejos.

## Ejemplos de Uso

El notebook principal ('TrabajoTopologia.ipynb') incluye casos de estudio prácticos:
1. **Homología del Anillo:** Verificación topológica de un espacio con 1 agujero ($\beta_1=1$).
2. **Análisis de Nubes de Puntos:** Detección de la topología subyacente en conjuntos de datos dispersos mediante persistencia homológica.

---
*Proyecto en desarrollo. Próximos pasos: Implementación de homología relativa y optimización de matrices dispersas.*
