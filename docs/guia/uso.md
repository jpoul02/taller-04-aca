# Uso básico de Next.js

Next.js se basa en archivos para crear rutas. Cada archivo en `pages/` representa una URL.

---

## Crear una página simple# Uso básico de Next.js

Next.js se basa en archivos para crear rutas. Cada archivo en `pages/` representa una URL.

---

## Crear una página simple

=== "JavaScript"

    ```jsx
    // pages/index.js
    export default function Home() {
      return <h1>Bienvenido a Next.js (JavaScript)</h1>
    }
    ```

=== "TypeScript"

    ```tsx
    // pages/index.tsx
    import type { NextPage } from 'next'

    const Home: NextPage = () => {
      return <h1>Bienvenido a Next.js (TypeScript)</h1>
    }

    export default Home
    ```

---

## Rutas dinámicas

Puedes usar corchetes para crear rutas con parámetros:

```jsx
// pages/blog/[slug].js
import { useRouter } from 'next/router'

export default function BlogPost() {
  const { slug } = useRouter().query
  return <h1>Publicación: {slug}</h1>
}
```

Navegar a `/blog/nextjs` mostrará: `Publicación: nextjs`.

---

## Crear una API

Next.js permite crear endpoints como si fueran funciones:

```js
// pages/api/hello.js
export default function handler(req, res) {
  res.status(200).json({ mensaje: 'Hola desde la API de Next.js' })
}
```

Accede en `http://localhost:3000/api/hello`

---

✅ Esto cubre creación de páginas, rutas dinámicas y endpoints API, todo sin configuración adicional.


=== "JavaScript"

    ```jsx
    // pages/index.js
    export default function Home() {
      return <h1>Bienvenido a Next.js (JavaScript)</h1>
    }
    ```

=== "TypeScript"

    ```tsx
    // pages/index.tsx
    import type { NextPage } from 'next'

    const Home: NextPage = () => {
      return <h1>Bienvenido a Next.js (TypeScript)</h1>
    }

    export default Home
    ```

---

## Rutas dinámicas

Puedes usar corchetes para crear rutas con parámetros:

```jsx
// pages/blog/[slug].js
import { useRouter } from 'next/router'

export default function BlogPost() {
  const { slug } = useRouter().query
  return <h1>Publicación: {slug}</h1>
}
```

Navegar a `/blog/nextjs` mostrará: `Publicación: nextjs`.

---

## Crear una API

Next.js permite crear endpoints como si fueran funciones:

```js
// pages/api/hello.js
export default function handler(req, res) {
  res.status(200).json({ mensaje: 'Hola desde la API de Next.js' })
}
```

Accede en `http://localhost:3000/api/hello`

---

✅ Esto cubre creación de páginas, rutas dinámicas y endpoints API, todo sin configuración adicional.
