# 📘 Guía Didáctica - CSS Básico

Este proyecto demuestra conceptos fundamentales de CSS para crear una página web estilizada con efectos visuales.

---

## 🎯 Conceptos de CSS Implementados

### 1. **Reset Universal con el selector `*`**

```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}
```

**¿Qué hace?**

- El selector `*` aplica estilos a TODOS los elementos HTML
- `box-sizing: border-box` → Hace que el ancho y alto incluyan padding y border (más predecible)
- `margin: 0` y `padding: 0` → Elimina espacios predeterminados del navegador
- `font-family` → Define la tipografía base para todo el documento

**💡 Por qué es importante:** Los navegadores tienen estilos predeterminados diferentes. Este reset crea una base consistente.

---

### 2. **Contenedor Principal - Layout Flexbox**

```css
.container {
  width: 70%;
  height: 100vh;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}
```

**Propiedades clave:**

- `width: 70%` → El contenedor ocupa el 70% del ancho de la pantalla
- `height: 100vh` → Altura completa de la ventana del navegador (vh = viewport height)
- `margin: 0 auto` → Centra horizontalmente el contenedor
- `display: flex` → Activa Flexbox para organizar elementos internos
- `flex-direction: column` → Apila elementos verticalmente (en columna)
- `align-items: center` → Centra elementos horizontalmente dentro del contenedor

**💡 Flexbox es una herramienta poderosa para crear layouts responsivos sin usar floats.**

---

### 3. **Estilización del Contenedor**

```css
.container {
  padding: 0 20px;
  border: 2px solid black;
  border-radius: 10px;
  background-color: rgb(146, 146, 146);
  background-size: cover;
}
```

**Propiedades visuales:**

- `padding: 0 20px` → Espacio interno: 0 arriba/abajo, 20px izquierda/derecha
- `border: 2px solid black` → Borde sólido negro de 2 píxeles
- `border-radius: 10px` → Esquinas redondeadas de 10px
- `background-color: rgb(146, 146, 146)` → Color de fondo gris
- `background-size: cover` → La imagen de fondo cubre todo el contenedor

**💡 Nota:** Hay código comentado que muestra cómo agregar una imagen de fondo con gradiente overlay.

---

### 4. **Tipografía y Efectos de Texto**

#### **Título Principal (h1)**

```css
h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  font-family: "Franklin Gothic Medium", Arial, sans-serif;
  font-style: italic;
  text-shadow: 2px 2px 4px #000000;
}
```

**Explicación:**

- `font-size: 2.5rem` → Tamaño relativo al tamaño base (1rem = 16px normalmente)
- `text-shadow: 2px 2px 4px #000000` → Sombra del texto
  - **2px** → Desplazamiento horizontal
  - **2px** → Desplazamiento vertical
  - **4px** → Difuminado de la sombra
  - **#000000** → Color negro

**💡 rem vs px:** rem es relativo y se adapta mejor a diferentes dispositivos.

#### **Subtítulo (h2)**

```css
h2 {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
  text-shadow: 2px 2px 4px #000000;
}
```

**Similar al h1 pero más pequeño**, mantiene la consistencia visual con el text-shadow.

#### **Párrafo (p)**

```css
p {
  font-size: 1.2rem;
  margin-bottom: 1rem;
  background-color: #fff;
  border-radius: 5px;
  color: orange;
}
```

**Contraste de color:**

- Fondo blanco (`#fff`) con texto naranja crea un contraste interesante
- `border-radius` suaviza las esquinas del fondo

---

### 5. **Estilos de Imagen**

```css
.img-bg {
  width: 40%;
  margin-top: 2rem;
}
```

**Imagen responsiva:**

- `width: 40%` → La imagen ocupa el 40% del contenedor padre
- Se adapta automáticamente a diferentes tamaños de pantalla

---

### 6. **Efectos de Hover y Transformaciones 3D** ⭐

```css
img:hover {
  transform: scale(1.1);
  transition: transform 0.5s;
  transform: rotateX(60deg);
  transform-style: preserve-3d;
}
```

**Análisis de efectos:**

- `img:hover` → Estilos aplicados cuando el mouse pasa sobre la imagen
- `transform: scale(1.1)` → Aumenta el tamaño al 110%
- `transition: transform 0.5s` → Animación suave de 0.5 segundos
- `transform: rotateX(60deg)` → Rotación en 3D sobre el eje X
- `transform-style: preserve-3d` → Mantiene la perspectiva 3D

**⚠️ Nota importante:** Hay múltiples declaraciones `transform` que se sobrescriben entre sí. Solo la última (`rotateX`) se aplicará.

**💡 Mejora sugerida:** Para combinar transformaciones, usa:

```css
transform: scale(1.1) rotateX(60deg);
```

---

## 🎨 Conceptos de Color

### **Diferentes formas de definir colores en CSS:**

1. **Nombre del color:** `black`, `white`
2. **Hexadecimal:** `#000000` (negro), `#fff` (blanco)
3. **RGB:** `rgb(146, 146, 146)` - Rojo, Verde, Azul
4. **Palabras clave:** `orange`

---

## 📊 Unidades de Medida Utilizadas

| Unidad | Ejemplo  | Descripción                                    |
| ------ | -------- | ---------------------------------------------- |
| `px`   | `2px`    | Píxeles - Valor absoluto                       |
| `%`    | `70%`    | Porcentaje - Relativo al elemento padre        |
| `rem`  | `2.5rem` | Relativo al tamaño de fuente raíz              |
| `vh`   | `100vh`  | Viewport height - % de la altura de la ventana |

---

## 🚀 Funcionalidades CSS Destacadas

### ✅ **Centrado con Flexbox**

El contenedor usa `display: flex` para centrar fácilmente todos sus elementos hijos.

### ✅ **Efectos de Sombra**

`text-shadow` añade profundidad y legibilidad al texto sobre fondos complejos.

### ✅ **Interactividad con `:hover`**

Mejora la experiencia del usuario con feedback visual.

### ✅ **Transformaciones CSS**

Efectos 3D sin necesidad de JavaScript.

---

## 🔧 Mejoras Potenciales

1. **Combinar transformaciones** en hover para aplicar escala y rotación simultáneamente
2. **Activar el gradiente comentado** para mejorar la legibilidad del texto sobre la imagen de fondo
3. **Añadir media queries** para mejorar la responsividad en dispositivos móviles
4. **Agregar más transiciones** para suavizar otros cambios de estado

---

## 📝 Estructura HTML Relacionada

El HTML utiliza:

- Un `<div class="container">` que envuelve todo el contenido
- Etiquetas semánticas: `<h1>`, `<h2>`, `<p>`, `<img>`
- Clase `.img-bg` para la imagen del logo

---

## 🎓 Recursos de Aprendizaje

- **Box Model:** Entender padding, border, margin
- **Flexbox:** Sistema de layout unidimensional
- **Transform:** Transformaciones 2D y 3D
- **Transition:** Animaciones suaves entre estados
- **Pseudo-clases:** `:hover`, `:focus`, etc.

---

**🎉 ¡Proyecto completado! Este ejemplo cubre los fundamentos esenciales de CSS para comenzar a crear páginas web atractivas.**
