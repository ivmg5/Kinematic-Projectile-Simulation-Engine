### **Serious Games - Motor de Simulación Cinemática de Proyectiles**

**Participantes:**  
- Santiago López Campos `A01643411`
- Fernanda Díaz Gutiérrez `A01639572`
- Diego Ivan Morales Gallardo `A01643382`
- Karen Corona Espinoza `A01642461`

#### **Contexto:**
El 3 de junio de 2018, el Volcán de Fuego hizo erupción en Guatemala, dejando un saldo de más de 300 personas muertas, numerosos heridos y miles de evacuados. Con el propósito de minimizar futuros incidentes fatales de esta naturaleza, la empresa Serious Games ha concebido el juego "Huehuetéotl - Dios del Fuego". El juego invita a los jugadores a rescatar sobrevivientes durante la erupción del volcán Popocatépetl. Una pieza clave de la mecánica del juego es el cálculo preciso de la trayectoria e impacto de los objetos sólidos lanzados por el volcán.

#### **Introducción:**
- Modelamos proyectiles de un volcán hipotético.
- Estudiamos diferentes métodos de representar la trayectoria de un proyectil, principalmente Verlet y Euler.
- Iniciamos determinando las sumatorias de fuerza, luego plasmamos estas ecuaciones en gráficas de excel y finalmente las implementamos en Matlab. Para nuestro proyecto, decidimos usar el método de Verlet.

#### **Investigación sobre características de las rocas:**

- **Densidad del aire promedio:** 1.826 kg/m^3
- **Valor de friccion:** 0.47

| Roca | Diámetro (m) | Masa (kg)  | Velocidad (m/s) | Ángulo (°) |
|------|--------------|------------|-----------------|------------|
| 1    | 0.06         | 0.260      | 300             | 25         |
| 2    | 3.5          | 62,860     | 300             | 70         |
| 3    | 0.1          | 1.257      | 300             | 30         |
| 4    | 1            | 1,300      | 300             | 40         |
| 5    | 2            | 10,894     | 300             | 45         |

#### **Modelo de Verlet: Elaboración de la ecuación**

\[ Fa = Bv^2 \]
\[ B = \frac{1}{2} \times \text{Densidad del aire} \times Cd \times A_{\text{transversal de la roca}} \]
\[ Fa = \left( \frac{1}{2} \times d \times Cd \times at \right) \times v^2 \]
\[ Mdv = \left( \frac{1}{2} \times d \times Cd \times dv \times t \right) \times v^2 \]

*Unidades:*  
- Densidad del aire: kg/m^3
- Área transversal: m^2
- Velocidad: m/s^2
- Fa Verlet: km m/s^2
- A = Área Transversal m^2
- B = Coeficiente de arrastre

#### **Modelo de Verlet: Ecuaciones utilizadas**

**Sumatoria de fuerzas:**
\[ Fx = -bvx \]
\[ Fy = mg-bvy \]
\[ axn = -\left( \frac{vxn}{|vxn|} \right) \times \left( \frac{b \times v^2 \times xn}{m} \right) \]
\[ ayn = -g-\left( \frac{vyn}{|vyn|} \right) \times \left( \frac{b \times v^2 \times yn}{m} \right) \]

**Ecuación de velocidad:**
\[ vxn = \frac{xn-x(n-1)}{deltat} \]
\[ vyn = \frac{yn-y(n-1)}{deltat} \]

**Ecuación de posición:**
\[ x(n+1) = 2xn-x(n-1)+0.5 \times axn \times deltat^2 \]
\[ y(n+1) = 2yn-y(n-1)+0.5 \times ayn \times deltat^2 \]

**Ecuación de posición para x(n-1):**
\[ x(n-1) = xn - (Vxn \times deltaT) \]
\[ y(n-1) = yn - (Vyn \times deltaT) + \left( \frac{1}{2} \right) \times ayn \times deltaT^2 \]

#### **Datos:**

Xo = 0 m  
Yo = 1000 m  
Dt = 1 s  
Vo = 300 m/s  
Ang = 42° (0.7330382858 en radianes)  
Cd = 0.11  
rho air (densidad) = 1.2 kg/m^3  
rho rock (densidad) = 4500 kg/m^3  
r = 1 m  
A = 3.141593 m^2  
V = 4.18879 m^3  
M = 18849.56 kg  
g = -9.81 m/s^2  
Vy = 200.7391819 m/s  
Vx = 222.9434476 m/s  
B = 0.207345138  

#### **Dificultades durante el desarrollo:**

Las principales dificultades enfrentadas durante el desarrollo de este proyecto incluyeron la realización de la sumatoria de fuerzas y la implementación de las trayectorias en el código.

#### **Conclusiones:**

Hemos logrado modelar con bastante precisión un volcán en erupción. Esta habilidad de programar modelaciones precisas puede ser extremadamente valiosa para prevenir tragedias y estimar fenómenos basados en datos históricos. A pesar de nuestro éxito, vemos áreas de mejora, donde el usuario podría ingresar más variables, afinando así los resultados y reduciendo el margen de error.
