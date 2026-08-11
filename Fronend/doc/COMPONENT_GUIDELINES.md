# 🎨 Guía de Arquitectura, Componentes y Estilos (Easy English)

Este documento contiene el contrato de diseño, arquitectura CSS y reglas de desarrollo para crear componentes en Astro + Tailwind CSS v4 en este proyecto sin alterar el diseño global.

---

## 🏛️ 1. Arquitectura de Temas y Colores

El proyecto utiliza **Tailwind CSS v4** con soporte nativo para variables semánticas mapping en `@theme`.

**REGLA DE ORO:** Queda **estrictamente prohibido** utilizar clases de colores fijos de Tailwind en componentes (ej. `bg-slate-900`, `text-white`, `border-gray-800`). Se deben utilizar **SIEMPRE** las utilidades de color semánticas definidas en el sistema.

```html
<!-- ❌ INCORRECTO: Color fijo (rompe el cambio de tema) -->
<div class="bg-slate-900 text-white border border-slate-800"></div>

<!-- ✅ CORRECTO: Utilidad semántica (reacciona al tema activo) -->
<div class="bg-surface text-primary border border-strong"></div>