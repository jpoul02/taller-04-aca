# Instalación de Next.js

Next.js ofrece una experiencia de desarrollo optimizada, rápida y sencilla desde el primer momento.

---

## Requisitos previos

| Herramienta | Versión recomendada | Verificar con |
|-------------|---------------------|----------------|
| Node.js     | ≥ 18.x              | `node -v`      |
| npm         | ≥ 9.x               | `npm -v`       |

---

## Crear un nuevo proyecto

Para crear tu aplicación con configuración inicial automática:

```bash
npx create-next-app@latest my-next-app
cd my-next-app
npm run dev
```

El generador te permitirá elegir:

- TypeScript o JavaScript
- Estilos con Tailwind CSS (opcional)
- ESLint y configuraciones adicionales
- Estructura con carpeta `src/` (recomendada)

---

## Estructura del proyecto

![Estructura del proyecto Next.js](../img/next.webp)

```plaintext
my-next-app/
├── public/         # Archivos estáticos (favicon, imágenes)
├── pages/          # Componentes con rutas automáticas
├── styles/         # Archivos CSS
├── node_modules/   # Dependencias
├── package.json    # Configuración de proyecto
├── next.config.js  # Configuración personalizada
└── tsconfig.json   # Solo si eliges TypeScript
```

> Si eliges la opción `src/`, los archivos estarán en `src/pages/`, `src/styles/`, etc.

---

## Scripts disponibles

| Comando         | Descripción                               |
|-----------------|--------------------------------------------|
| `npm run dev`   | Inicia el servidor de desarrollo           |
| `npm run build` | Genera archivos para producción            |
| `npm run start` | Inicia el servidor en modo producción      |

---

📎 Continúa con la [guía de uso de Next.js](uso.md) para escribir tus primeras páginas y rutas dinámicas.
