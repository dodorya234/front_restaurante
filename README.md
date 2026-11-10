# ProyectoRestaurante

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 22.2.3.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Vitest](https://vitest.dev/) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Catálogo basado en APIs

El menú consume directamente [TheMealDB](https://www.themealdb.com/api.php) y [TheCocktailDB](https://www.thecocktaildb.com/). El componente `Api` carga los catálogos al iniciar la aplicación y permite reintentar si una API falla. `ApiMenuService` reúne los resultados por letra con concurrencia limitada y reintentos; `ProductosService` normaliza, cachea y comparte los productos con las especialidades, las páginas de comidas y bebidas, los pedidos y el juego.

Las comidas se muestran agrupadas por categoría y permiten buscar por nombre e ingrediente. Las bebidas permiten buscar por nombre e ingrediente, además de filtrar por tipo y categoría. Los precios se asignan aleatoriamente entre USD 5 y USD 20, y se mantienen iguales para cada producto durante la sesión.

Se requiere conexión a internet para cargar el catálogo. Si una API no está disponible, cada página informa del error y permite reintentar.

## Organización del código

Los componentes coordinan la interfaz y los servicios gestionan la carga de datos. Los modelos de `src/app/models` representan productos y pedidos; `ReciboPdfService` genera el recibo descargable sin mezclar esa responsabilidad con el componente del pedido.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.
