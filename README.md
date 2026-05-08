# 🎮 Pygame Project Boilerplate

Esta es una plantilla base estructurada para el desarrollo de videojuegos en Python utilizando la librería **Pygame**. Está diseñada bajo el paradigma de **Programación Orientada a Objetos (POO)** para facilitar la escalabilidad y el orden en proyectos educativos.

## 📋 Requisitos

Para ejecutar esta plantilla, necesitas tener instalado Python y la librería Pygame:

```bash
pip install pygame

## 🎮 Pygame Boilerplate: Guía de Inicio

Esta es una plantilla base estructurada para el desarrollo de videojuegos en Python utilizando la librería Pygame. Está diseñada bajo el paradigma de Programación Orientada a Objetos (POO) para facilitar la escalabilidad y el orden en proyectos educativos de Algorithmics.

📋 Requisitos e Instalación

Para ejecutar este código, asegúrate de tener instalado Python y la librería Pygame en tu entorno local:

pip install pygame


🏗️ Arquitectura de la Plantilla

El código se divide en 5 secciones clave que todo desarrollador debe conocer para mantener un flujo de trabajo profesional:

1. Inicialización

Activación de los módulos principales de Pygame:

init(): Prepara el núcleo de la librería.

font.init(): Habilita el uso de fuentes de texto.

mixer.init(): Permite la reproducción de sonidos y música.

2. Configuración (Constantes)

Uso de variables globales fijas para el control del entorno:

ANCHO y ALTO: Definen las dimensiones de la ventana de juego.

FPS: Frames por segundo (fijado en $60$ para una fluidez estable).

COLOR_FONDO: Definido en formato RGB (Red, Green, Blue).

3. Sistema de Clases (Sprites)

GameSprite: La clase base. Gestiona la imagen, el rectángulo (rect) para colisiones y el método reset() para dibujar en pantalla.

Player: Hereda de GameSprite. Incluye la lógica de control por teclado (W, A, S, D).

Enemy: Hereda de GameSprite. Diseñada para movimiento automático o patrones de patrullaje.

4. Instanciación

Espacio dedicado a crear los objetos reales del juego (jugadores, enemigos, proyectiles) y organizar los Grupos de Sprites antes de que comience la acción.

5. Game Loop (Ciclo Principal)

El corazón del programa, dividido en tres fases continuas:

Gestión de Eventos: Detección de cierre de ventana y teclas especiales (como R para reiniciar).

Lógica del Juego: Donde se actualizan las posiciones y se verifican las colisiones mediante if not finish:.

Renderizado: Proceso de limpiar la pantalla con window.fill() y dibujar los nuevos estados de los objetos.

📝 Instrucciones para Estudiantes

Sigue estas indicaciones para completar tu proyecto sobre esta base:

🚀 Tareas Iniciales

Carga de Imágenes: Asegúrate de tener archivos .png o .jpg en la carpeta del proyecto y descomenta las líneas de instanciación del objeto player.

Lógica de Movimiento: Recuerda que en Pygame el punto $(0,0)$ es la esquina superior izquierda. El eje $Y$ crece hacia abajo. Para subir, restamos a rect.y; para bajar, sumamos.

Detección de Colisiones: Utiliza el método sprite.collide_rect() o sprite.spritecollide() dentro de la sección de lógica para activar el estado finish = True.

🛡️ Buenas Prácticas

Nombres Descriptivos: Mantén los nombres de las constantes en MAYÚSCULAS para diferenciarlas de las variables que cambian.

Modularidad: Evita escribir lógica compleja directamente en el while. Define métodos nuevos dentro de tus clases y llámalos usando .update().

Reinicio Eficiente: Implementa la lógica necesaria dentro del evento KEYDOWN con la tecla K_r para resetear las coordenadas de tus sprites al estado inicial.

Plantilla desarrollada para fines educativos en Algorithmics.
