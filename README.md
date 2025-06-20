# 🧩 Printorium Landing – Diseño Web con CSS Moderno

Este proyecto es una landing page estática desarrollada con **HTML** y **CSS moderno**, cuyo objetivo principal es mostrar diseño visual responsivo y actual sin interactividad funcional. El enfoque fue implementar nuevas características de CSS puro aplicadas a una interfaz inspirada en un diseño tomado de **Figma Community (free template)**.

---

## 🎨 Stack utilizado

- HTML5 (estructura básica, sin JavaScript)
- CSS moderno (sin frameworks ni preprocessors)

---

## 🚀 Características implementadas

### ✅ 1. `container-type` y `@container`

Se utilizó `container-type: inline-size;` en contenedores clave para habilitar **container queries**. Esto permite que los componentes se adapten a su **contenedor padre**, no al viewport global, mejorando la modularidad.

**Implementado en:**

```css
.container {
  container-type: inline-size;
}

```
---

### ✅ 2. color-mix() y linear-gradient() para fondo dinámico

La sección .features utiliza un degradado dinámico generado con color-mix() que parte del color principal (--color-accent) y se mezcla con negro.

**Código aplicado:**

```css
.features {
  padding: 4rem 0;
  background: linear-gradient(
    135deg,
    color-mix(in srgb, var(--color-accent) 40%, black) 0%,
    color-mix(in srgb, var(--color-accent) 5%, black) 100%
  );
}
```
Esto genera un fondo moderno, suave y consistente con la identidad visual.
---

### 3. Grid layout responsivo con auto-fit y minmax()

Para la sección de features y disposición de tarjetas se usó:

```css
.grid-4 {
  display: grid;
  gap: var(--gap);
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
}
```

Esto asegura que las cards se distribuyan automáticamente y de forma fluida en pantallas pequeñas sin necesidad de media queries adicionales.

---

### 4. Variables CSS Globales (:root)

El sistema de diseño está gestionado mediante variables centralizadas para mantener consistencia:

```css
:root {
  --color-bg: #0a0a0a;
  --color-text: #f5f5f5;
  --color-accent: #c2ff00;
  --color-muted: #888;
  --max-width: 1200px;
  --gap: 2rem;
  --font-main: 'Inter', sans-serif;
}
```

Variables como --color-accent también fueron utilizadas para mezclas dinámicas con color-mix().

---

### 5. Diseño responsivo sin media queries globales

Gracias a container queries, los componentes como .hero y .feature-card responden a su ancho interno, eliminando la necesidad de media queries generales y mejorando la escalabilidad del diseño modular.

### ✅ 6. Proyecto basado en Figma Community

El diseño fue inspirado en una plantilla gratuita de **Figma Community**. Se respetaron:

- Tipografías y jerarquías  
- Paleta de colores  
- Estructura visual  
- Distribución de secciones y estilo general

> ⚠️ Nota: Este proyecto no implementa lógica JavaScript. Está centrado exclusivamente en mostrar capacidades visuales con CSS moderno.

---

### 🗂 Archivos del proyecto

- `index.html` – estructura semántica del sitio  
- `style.css` – lógica visual y estilos modernos  
- `escultura1.png` – imagen renderizada usada en el hero  
- `home.png` – mockup completo de referencia visual  

---

### ✨ Resultado visual

Diseño adaptativo, moderno y limpio con características de CSS de última generación:

- `@container` + `container-type`  
- `color-mix()` con `linear-gradient()`  
- Layout fluido con Grid moderno  
- Variables CSS y estructura clara  

---

### 📸 Vista previa

*(incluir imagen aquí si es necesario)*

---

### 🧪 Soporte requerido

Para visualizar correctamente las características modernas, se recomienda:

- Navegadores modernos actualizados:
  - Chrome 111+
  - Firefox 110+
  - Safari 16.4+
- Soporte para `@container` y `color-mix()`

---

### 🧾 Licencia

Este proyecto utiliza un diseño gratuito de **Figma Community** y es solo con fines de aprendizaje y exhibición personal.
