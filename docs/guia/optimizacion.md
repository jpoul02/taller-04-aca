# Optimizaciones avanzadas en Next.js

Next.js incluye herramientas para mejorar el rendimiento de tus aplicaciones web con muy poca configuración adicional.

---

## Optimización de imágenes

Next.js incluye el componente `<Image />`, que permite:

- Carga diferida (lazy loading)
- Compresión automática
- Soporte para WebP y AVIF
- Redimensionamiento automático

```jsx
import Image from 'next/image'

export default function Perfil() {
  return (
    <Image
      src="/perfil.jpg"
      alt="Foto de perfil"
      width={200}
      height={200}
    />
  )
}
```

---

## Uso de `getStaticProps` y `getServerSideProps`

Estas funciones permiten definir cómo y cuándo se renderiza una página:

| Función              | Momento de ejecución | Cuándo usarla                         |
|----------------------|----------------------|---------------------------------------|
| `getStaticProps`     | En build             | Datos que no cambian con frecuencia   |
| `getServerSideProps` | En cada request      | Datos que cambian constantemente      |

---

## Middleware y headers

Con Next.js puedes interceptar rutas y modificar headers desde el archivo `middleware.js`.

```js
// middleware.js
export function middleware(request) {
  const response = NextResponse.next()
  response.headers.set('x-mi-header', 'valor')
  return response
}
```

---

📎 Vuelve a la [guía de uso](uso.md) para seguir creando componentes.
