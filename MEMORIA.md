# Memoria Técnica: Generador de Contraseñas Seguras (Web)

## 🎯 Objetivo del Proyecto

El principal objetivo de este proyecto fue crear una herramienta accesible y fácil de usar para generar contraseñas de alta entropía. Al implementar la interfaz con tecnologías web (HTML, CSS, JavaScript), se logró un producto final **visible** y directamente utilizable en el navegador, ideal para demostrar habilidades de desarrollo front-end.

## 🛠️ Stack Tecnológico

| Tecnología | Rol | Uso Específico |
| :--- | :--- | :--- |
| **HTML5** | Estructura | Definición de la interfaz, *inputs* para longitud, y *checkboxes* para los tipos de caracteres. |
| **CSS3** | Presentación | Estilos básicos, centrado de la aplicación, y diseño receptivo (*responsive*) para mejorar la visibilidad. |
| **JavaScript (Vanilla JS)** | Lógica Central | Manejo del DOM, gestión de eventos (clic en generar/copiar) y la lógica de aleatoriedad para la generación de la contraseña. |

## 🧠 Lógica de Generación de Contraseñas

1.  **Definición de Conjuntos:** Se definen cuatro cadenas constantes (`MINUSCULAS`, `MAYUSCULAS`, `NUMEROS`, `SIMBOLOS`) para agrupar todos los caracteres posibles.
2.  **Construcción del *Pool*:** Una cadena única (`caracteresPool`) se construye dinámicamente, sumando los conjuntos seleccionados por el usuario mediante los *checkboxes*.
3.  **Aleatoriedad:** Se utiliza `Math.random()` para seleccionar un índice aleatorio dentro del `caracteresPool` en cada iteración del bucle, garantizando que cada carácter tenga una probabilidad igual de ser elegido.
4.  **Generación Final:** La contraseña se concatena carácter por carácter hasta alcanzar la longitud especificada por el usuario.

## ✨ Características Implementadas

* **Longitud Personalizable:** El usuario puede definir la longitud exacta de la contraseña (entre 4 y 50 caracteres).
* **Tipos de Caracteres Seleccionables:** Control total sobre si incluir mayúsculas, números y símbolos.
* **Copia al Portapapeles:** Implementación de la API `navigator.clipboard.writeText()` para copiar la contraseña con un solo clic.
* **Validación de Entrada:** Se verifica que la longitud sea un número válido y mayor a 4.

---
