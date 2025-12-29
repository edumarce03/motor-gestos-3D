# 🚀 Interactive 3D particles

Un ecosistema de partículas interactivo de alto rendimiento que fusiona **Visión Artificial** y **Renderizado 3D** en tiempo real. Este proyecto permite a los usuarios manipular estructuras matemáticas complejas mediante gestos naturales capturados por la cámara.

---

## ✨ Características Principales

- **🕹️ Control Gestual:** Manipulación fluida del sistema de partículas mediante el seguimiento de la palma de la mano.
- **🤏 Sensor de Tensión:** Las partículas reaccionan a la apertura y cierre de la mano, contrayéndose o expandiéndose dinámicamente.
- **🎨 UI Adaptativa:** Interfaz de control minimalista con selector de color que sincroniza la estética de las partículas con los elementos activos de la UI.
- **🔮 5 Plantillas Matemáticas:**
  - **Saturno:** Esfera central rodeada por un sistema de anillos planos.
  - **Fuegos:** Distribución esférica aleatoria con efecto de explosión.
  - **Galaxia:** Basada en la espiral de Arquímedes con múltiples brazos.
  - **Mobius:** Representación tridimensional de la famosa cinta topológica de una sola cara.
  - **Cubo:** Distribución uniforme en las seis caras de un cubo de datos.

## 🛠️ Tecnologías

Este proyecto utiliza un stack de vanguardia para garantizar fluidez (60 FPS):

- **[Three.js](https://threejs.org/):** Motor de WebGL para el renderizado de las 18,000 partículas.
- **[MediaPipe Hands](https://google.github.io/mediapipe/):** Framework de ML para la detección de landmarks de la mano.
- **[Lucide Icons](https://lucide.dev/):** Set de iconos vectoriales para una UI limpia.
- **Google Camera Utils:** Optimización del flujo de video para procesamiento de datos.

## 🚀 Instalación y Uso

1.  **Descarga** el archivo `index.html`.
2.  **Abre** el archivo en un navegador moderno (Chrome, Edge o Brave recomendados).
3.  **Permisos:** Acepta el uso de la cámara cuando el navegador lo solicite.
4.  **Interacción:**
    - **Movimiento:** Mueve tu mano para desplazar el sistema en los ejes X e Y.
    - **Escala:** Cierra la mano (unir dedos) para comprimir la forma; ábrela para expandirla.
    - **Personalización:** Usa el panel superior para cambiar el color y alternar entre las geometrías.

## 🧠 Detalles Técnicos

El sistema utiliza **Interpolación Lineal (Lerp)** para las transiciones entre formas, permitiendo que cada partícula viaje desde su posición actual a su nuevo objetivo de forma suave, sin saltos bruscos. El rendimiento se mantiene óptimo gracias al uso de `BufferAttributes`, minimizando el overhead de comunicación entre la CPU y la GPU.

```javascript
// Ejemplo de la lógica de transición utilizada
currentPositions[i] += (targetPositions[i] - currentPositions[i]) * 0.08;
```
