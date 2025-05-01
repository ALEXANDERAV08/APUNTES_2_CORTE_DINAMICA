# APUNTES_2_CORTE_DINAMICA
## correcion parcial 1 corte 
## 2.1 retroalimentacion tema 2:
## 📚 Ejercicio 1:
$$2\ddot{x} + 2\dot{x} + x = 1\$$  

**con las condiciones iniciales:**  $x(0) = 0,\quad \dot{x}(0) = 2$

**Aplicando Transformada de Laplace:**

$$2[s^2 X(s) - s x(0) - \dot{x}(0)] + 2[s X(s) - x(0)] + X(s) = \frac{1}{s}$$

**sustituyendo condiciones iniciales:**

$$2[s^2 X(s) - 2] + 2[s X(s)] + X(s) = \frac{1}{s}$$

$$2s^2 X(s) - 4 + 2s X(s) + X(s) = \frac{1}{s}$$

$$X(s)(2s^2 + 2s + 1) = \frac{1}{s} + 4$$

$$X(s) = \frac{1 + 4s}{s(2s^2 + 2s + 1)}$$

**Aplicando fracciones parciales:** 

$$\frac{1 + 4s}{s(2s^2 + 2s + 1)} = \frac{A}{s} + \frac{Bs + D}{2s^2 + 2s + 1}$$

**Determinación de A:**

$$1 + 4s = A(2s^2 + 2s + 1) + (Bs + D)s$$

**al evaluar s= 0**

$$A = \frac{1 + 4(0)}{2(0)^2 + 2(0) + 1} = \frac{1}{1} = 1$$

**Al evaluar s = -1 + 2i**

$$\frac{1 + 4(-1 + 2i)}{-1 + 2i}  = (-1 + 2i)(B(-1 + 2i) + D)$$

$$\frac{1 + 4(-1 + 2i)}{-1 + 2i}  = -B+ 2Bi + D$$

$$\frac{1 + 4 + 8i}{-1 + 2i} * \frac{-1 + 2i}{-1 + 2i} = -B+ 2Bi + D$$

$$\frac{3 + 6i + 8i + 16}{5} = -B + 2Bi + 5$$

$$\frac{19}{5} = -B - D$$

$$\frac{2i}{5} = 2Bi$$

$$B=\frac{1}{5}$$
$$D=\frac{20}{5} = 4$$
$$A = 1$$

## 📚 Ejercicio 2:

Determinar la función en el dominio del tiempo de F(s):

$$\frac{6S}{(S-\frac{5}{2})(S^2 -4S + 8)}$$

**Aplicando fracciones parciales:**

$$\frac{6S}{(S-\frac{5}{2})(S^2 -4S + 8)} = \frac{A}{S-\frac{5}{2}} + \frac{Bs + C}{S^2-4S+8}$$

**multiplicamos ambos lados por el denominador comun para eliminar los denominadores**

**Expandimos y agrupamos terminos semejantes**

$$6s= As^2 - 4As + 8A + Bs^2 - \frac{5}{2} Bs + Cs - \frac{5}{2}C$$

$$6s= (A+B)s^2 + (-4A - \frac{5}{2}B + C)s + (8A - \frac{5}{2}C) - \frac{5}{2}C$$

**Igualamos los coeficientes de ambos lados:**

**coeficiente de s^2:**

$$A+B=0$$
$$B = -A$$

**Coeficiente de s:**

$$-4A - \frac{5}{2}B + C = 6$$

**Termino independiente**

$$8A - \frac{5}{2}C=0$$

**Sustituimos B=A en la segunda ecuacion:**

$$-4A - \frac{5}{2} (-A) + C = 6$$

$$-4A \frac{5}{2}A + C = 6$$

$$-\frac{8}{2}A + \frac{5}{2}A+C=6$$

**Ecuacion 1:**

$$-\frac{3}{2}A + C = 6 $$

**Ecuacion termino independiente:**

$$8A - \frac{5}{2}C=0$$

$$8A = \frac{5}{2}C$$
**Ecuecion 2:**

$$C=\frac{16}{5}A$$

**Sustituimos $C = \frac{16}{5}A$ en la Ecuación 1:**

$$-\frac{3}{2}A + \frac{16}{5}A = 6$$

$$-(\frac{15}{10}A+\frac{32}{10})A = 6$$

$$\frac{17}{10}A=6$$

$$A = \frac{60}{17}$$

**Entonces**

$$B = -A = -\frac{60}{17}$$

$$C = \frac{16}{5} \cdot \frac{60}{17} = \frac{960}{85} = \frac{192}{17}$$

**Por lo tanto, la descomposición en fracciones parciales es:**

$$F(s) = \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} + \frac{-\frac{60}{17}s + \frac{192}{17}}{s^2 - 4s + 8}$$

**Simplificamos:**

$$F(s) = \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60}{17} \cdot \frac{s - \frac{192}{60}}{s^2 - 4s + 8}$$

$$F(s) = \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60}{17} \cdot \frac{s - \frac{16}{5}}{s^2 - 4s + 8}$$

**Para el término $s^2 - 4s + 8$ completamos el cuadrado:**

$$s^2 - 4s + 8 = (s^2 - 4s + 4) + 4 = (s - 2)^2 + 4$$

**Por lo tanto:**

$$F(s) = \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60}{17} \cdot \frac{s - \frac{16}{5}}{(s - 2)^2 + 4}$$

**Separamos el segundo término en dos partes para facilitar la transformada inversa:**

$$\frac{s - \frac{16}{5}}{(s - 2)^2 + 4} = \frac{s - 2}{(s - 2)^2 + 4} + \frac{-2 + \frac{16}{5}}{(s - 2)^2 + 4}$$

$$= \frac{s - 2}{(s - 2)^2 + 4} + \frac{\frac{6}{5}}{(s - 2)^2 + 4}$$

**Entonces:**

$$F(s) = \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60}{17} \left( \frac{s - 2}{(s - 2)^2 + 4} + \frac{6}{5} \cdot \frac{1}{(s - 2)^2 + 4} \right)$$

**Distribuyendo:**

$$F(s) = \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60}{17} \cdot \frac{s - 2}{(s - 2)^2 + 4} - \frac{60}{17} \cdot \frac{6}{5} \cdot \frac{1}{(s - 2)^2 + 4}$$

$$= \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60}{17} \cdot \frac{s - 2}{(s - 2)^2 + 4} - \frac{72}{17} \cdot \frac{1}{(s - 2)^2 + 4}$$

**Aplicando transformada inversa de Laplace:**

$$f(t) = \frac{60}{17} e^{\frac{5}{2}t} - \frac{e^{2t}}{17} \left(60 \cos(2t) + 36 \sin(2t) \right)$$


## 1 Sistemas Mecanicos

​Un sistema mecánico es un conjunto de componentes físicos interconectados cuya función principal es transformar o transmitir movimiento y fuerza desde una fuente de energía hasta un punto de salida, permitiendo así la realización de un trabajo específico.
### 1.1 Sistema masa-resorte-amortiguador

Un sistema masa-resorte-amortiguador es un modelo mecánico fundamental que describe cómo una masa se mueve bajo la influencia de fuerzas elásticas y de amortiguamiento. Este sistema es un modelo clasico en la mecanica que describe el comportamiento de un objeto (masa) que esta sujeto a la accion de un resorte y un amortiguador. Este sistema es fundamental para entender para entender como las fuerzas afectan el movimiento de objetos y como se disipa la energia en sistemas reales

### 1.2 Componentes principales

- **Masa(m):** Representa el objeto que se mueve bajo la influencia de las fuerzas del resorte y el amortiguador.
- **Resorte(k):** Aplica una fuerza proporcional a la deformacion del resorte, segun ley de hooke. Esta fuerza tiende a devolver la masa a su poscición de equilibrio. La constante del resorte mide la rigidez del mismo.
- **Amortiguador(B):** Representa la ressitencia que disipa energia, como la fricion o un amortiguador real, su función es reducir la velocidad del sistema con el tiempo. La fuerza de amortiguamiento es proporcional a la velocidad de la masa.
- **Fuerza externa F(t):** Es cualquier fuerza que se apliquye desde el exterior, como una fuerza constante o periodica. 

### 1.3 Ecuacion del movimiento

La dinámica del sistema se describe mediante una ecuación diferencial de segundo orden $m\ddot{x}(t) + b\dot{x}(t) + kx = F(t)\$ 

## 2 Sistemas Acoplados 

Los sistemas acoplados son aquellos en los que dos o mas sistemas interactúan entre sí, influyendo mutuamente en su comportamiento. Estos sitemas están conectados de tal forma que el movimiento o la dinámica de un sistema afecta directamente al otro, lo que genera una relación interdependiente

### 2.1 Caracteristicas de los sistemas acoplados
- **Interaccion:** los sistemas no son independientes, las variables que describen uno de los sitemas influyen en las variables del otro.
- **Ecuaciones interrelacionadas:** Las ecuaciones que describen cada sistema están vinculadas. es decir, las ecuaciones diferenciales o algebraicas de un sistema contienen términos que dependen de las variables del otro sistema.
- **Transferencia de energia:** Existe una transferencia de energia, fuerza o información entre los sistemas. esto puede ser a través de fuerzas fisicas (como una conexión elástica o un amortiguador) o señales de otro tipo.

### 2.2 Ecuaciones en sistemas acoplados 

las ecuaciones diferenciales que describren estos sistemas suelen ser de la forma:

$m_1\ddot{x_1} + d_1\dot{x_1} + k_1x_1 - k_2(x_2-x_1) = F_1(t)\$ 

$m_2\ddot{x_2} + d_2\dot{x_2} + k_2(x_2-x_1) = F_2(t)\$ 

aqui $x_1$ y $x_2$ representan el desplazamiento de cada masa, $k_2$ es la cosnstante del resorte que conecta las dos masas, y $f_1(t)$ y $f_2(t)$ son las fuerzas externas aplicadas a cada masa. Las ecuaciones estan interconectadas por que el movimiento de una masa afecta directamente a la otra.

# 📚 Ejercicio masa-resorte-amortiguador

Obtener las ecuaciones diferenciales del siguiente sistema 
![image](https://github.com/user-attachments/assets/ba02c2d3-3465-40e8-b9e0-e8a318840834)


**Se procede a realizar el diagrama de fuerzas para cada masa (Diagrama de cuerpo libre)

**Para masa 2:**

![image](https://github.com/user-attachments/assets/fc3dab1e-3f57-476a-a1d6-b6f01a37c325)


$$fb+fk-ff=0$$
$$b(\dot{y_2(t)} - \dot{y_1(t)}) + k(y_2(t) - y_1(t))= 0$$
$$b(\dot{y_2(t)} - \dot{y_1(t)}) + k(y_2(t) - y_1(t))= m*a$$
**Donde a = $\frac{d^2y(t)}{dt^2}$ que tambien se puede respresentar como $\ddot{y}$**

**sabiendo esto tenemos:**

$$b(\dot{y_2(t)} - \dot{y_1(t)}) + k(y_2(t) - y_1(t))= = m_2*\ddot{y}$$

**Para masa 1:**

![image](https://github.com/user-attachments/assets/15612b6a-3e37-492a-adcc-3fd46a156a49)

$$f(t)-fk-fb=0$$
$$f(t)- b(\dot{y_1(t)} - \dot{y_2(t)}) - k(y_1(t) - y_2(t)) = m_1*\ddot{y}$$

## 2 SISTEMAS ROTACIONALES
Los sistemas rotacionales son otro tipo de sistemas mecanicos solo que en este caso lo que varia es la fuerza aplicada ya que es un movimiento circular que nos genera un torque,estos sistemas se analizan usando las leyes del movimiento rotacional, que son parecidas a las del movimiento traslacional pero en términos angulares.

![image](https://github.com/user-attachments/assets/9e5ba5dd-1701-4749-8064-39ca76fd514d)

Para el anaisis de estos sistemas usaremos leyes comparables al movimiento lineal tales como la fuerza de rosamiento donde el angulo $\varphi$ es el angulo de torcion.
$$F_r = k*\varphi$$

Tambien tendremos la fuerza de friccion donde la $\frac{\mathrm{d}\varphi }{\mathrm{d} t}$ es la velocidad angular del sistema
$$F_{f}=b*\frac{\mathrm{d}\varphi }{\mathrm{d} t}$$
y por ultimo el torque donde la constante j es el momento de inercia del sistema 

$$T=j*\frac{\partial \varphi ^2 }{\partial t^2}$$

Deigual forma como se venia trabajando para los demas sistemas este tambien lo anamizaremos por medio de un diagrama de cuerpo libre el cual nos quedara de la siguiente forma ya con las fuerzas dibujadas para asi poder generar la funcion correspondiente.

💡**Ejemplo:**
![image](https://github.com/user-attachments/assets/5180bf33-115c-42fb-9293-3210f8cc7aa8)

Una vez con esto podremos hacer la funcion teniendo que $\sum T=J*\alpha$ para ello tendremos que:

$$T-F_{R}-F_{F}=j*\alpha$$
Remplazando tendriamos que la funcion no quedaria de la siguiente forma.

$$T(t)-K\theta (t)-B\frac{\partial \theta(t)}{\partial t}=J\frac{\partial^2\theta (t) }{\partial t^2}$$

## 2.1 Conversion Movimiento Translacional-Rotacional
Para estos sistemas veremos el proceso mediante el cual se convierte un desplazamiento lineal en un desplazamiento angular o a la inversa todo esto mediante un sistema mecanico el cual puede ser desglosado en varias partes las mas comunes son:
### Poleas y correas
Transmiten movimiento rotacional a uno lineal o al contrario a través de una banda o varias bandas.
### Cremallera y piñón
Convierte el movimiento rotacional de un engranaje en movimiento lineal.
### Tornillos sin fin 
Convierte la rotación de un tornillo dada ya sea por un motor o un giro manual en movimiento lineal.

💡**Ejemplo:** Tenemos el siguiente sistema combinando el cual es un motor enganchado a una polea para a si poder mover la caja.

![image](https://github.com/user-attachments/assets/80f14a08-aa53-4ce4-a5bb-5852d78c2775)

Teniendo esto como base pasaremos al diagrama de cuerpo libre obteniendo a si las fuerzas positivas y negativas del sistema.

![image](https://github.com/user-attachments/assets/c8dc6e37-972a-4a1a-bf99-5ecab4da4df7)

Con esto pasaremos a resolver la $\sum T=J*\alpha$ teniendo asi:

$$T_{m}-T_{1}-T_{F}=J_{m}*\alpha$$

Donde remplazando las incognitas por sus funciones obtendremos el siguiente resultado, sabiendo que para $T_{1}$ el momento de inercia es $mr^{^2}$.

$$T_{m}-mr^{^2}\frac{\partial^2\theta  }{\partial t^2}-B\frac{\partial \theta }{\partial t}=J_{m}\frac{\partial^2\theta  }{\partial t^2}$$

Teniendo en cuenta que el $\theta = y/r$ remplazamos en la ecuacion

$$T_{m}-mr\frac{\partial^2 y}{\partial t^2}-\frac{B}{r}\frac{\partial y }{\partial t}=\frac{J_{m}}{r}\frac{\partial^2 y}{\partial t^2}$$

## 3 CIRCUITOS RLC
Un circuito RLC es un circuito eléctrico que está formado por resistencias inductancias y capacitancias estas a su vez están conectadas en serie o en paralelo también pueden ser circuitos mixtos son fundamentales para los sistemas de control filtrado de señales y otros circuitos electrónicos.

![image](https://github.com/user-attachments/assets/bfbdd38f-73fe-4780-82c3-9c42bf77f4ca) 

💡**Ejemplo 2:**
![image](https://github.com/user-attachments/assets/c25c2e1c-5cd9-41b0-a014-92bb979aec6c)

Estos circuitos se rigen bajo la ley de ohm y otras leyes más como podemos ver en las siguientes ecuaciones tenemos que para cada uno de los elementos tenemos una ecuación característica estas son las siguientes.

$$R=\frac{V(t)}{I(t)}$$
$$I= C\frac{dV(t)}{dt}$$
$$V= L\frac{di(t)}{dt}$$

Teniendo en cuenta estas ecuaciones y la imagen anterior podemos resolver el ejemplo 2 el cual sería la solución del circuito en serie, para ello utilizaremos la ley de voltajes de kirchhoff para así poder solucionar y encontrar la ecuación que nos describe el sistema.

Iniciaremos haciendo la suma de voltajes e igualando a cero.

$$V_i + V_R + V_L V_C = 0$$

Luego reemplazaremos las ecuaciones mostradas anteriormente en la ecuación.

$$V_i (t) + i(t)R + L\frac{di(t)}{dt} + V_C = 0$$

Una vez teniendo esto nos podemos dar cuenta que para que nos quede todo el factor es de voltaje del condensador reemplazaremos en la derivada de $i(t)$ por lo que vale $I$, teniendo la siguiente ecuación.

$$-U(t)+RC\frac{\mathrm{d}V_{C}(t)}{\mathrm{d} t}+LC\frac{\mathrm{d^2}V_{C}(t)}{\mathrm{d}t^2}+V_{C}=0$$



