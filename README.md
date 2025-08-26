# SportStore

Aplicación demo de e‑commerce construida con Angular 13. Permite explorar productos, filtrarlos por categoría, paginarlos, ver detalles, gestionar un carrito de compras y completar un proceso de checkout. Incluye ruteo con guards, módulos de características y un backend simulado con json-server.

## Características principales

- Catálogo de productos:
    - Listado de productos con detalles.
    - Filtrado por categoría.
    - Paginación del listado de productos.
- Carrito de compras:
    - Agregar, eliminar y actualizar cantidades.
    - Resumen rápido de carrito y vista de detalle del carrito.
- Checkout y órdenes:
    - Modelo de órdenes y flujo de compra.
- Navegación y seguridad:
    - Rutas configuradas para tienda, carrito y checkout.
    - Guard de rutas que protege el flujo de navegación.
- Arquitectura modular:
    - Módulo Store (presentación y navegación).
    - Módulo Model (modelos, repositorios y datasource).
    - Directiva personalizada para contadores en UI.
- Backend simulado:
    - API falsa con json-server y middleware de autenticación para endpoints protegidos.

## Tecnologías

- Angular 13, TypeScript 4.4
- RxJS, Bootstrap 5
- json-server para datos simulados

## Requisitos

- Node.js y npm
- Angular CLI 13

## Configuración y ejecución

1) Instalar dependencias: ```npm install```

2) Iniciar backend simulado (json-server): ```npm run json-server```
### Alternativa directa
```npx json-server data.js -p 3500 -m authMiddleware.js```

3) Iniciar servidor de desarrollo Angular: ```npm start``` o ```ng serve```


4) Abrir la app:
- http://localhost:4200/

## Estructura de módulos (alto nivel)

- Módulo Model:
    - Modelos de dominio: Producto, Carrito, Orden.
    - Repositorios: acceso a productos y órdenes.
    - Datasource estático: integración con json-server.
- Módulo Store:
    - Componentes: tienda, resumen de carrito, detalle de carrito, checkout.
    - Directiva personalizada para control de contadores.
    - Ruteo propio e integración con el ruteo raíz.
- Guarda de rutas:
    - Protege el acceso directo a rutas para mantener el flujo desde la tienda.

