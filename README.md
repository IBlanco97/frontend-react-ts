El primer paso para la creacion de este proyecto fue ejecturar
```
npm create vite@latest
```
seleccionando el framework React con las tecnologías 
* TypeScript:
Lo elijo por encima de JavaScript porque el tipado fuerte hace el codigo mas legible, reutilizable. Mejora el autocompletado. El compilador señala errores de tipado que serían bugs más complicados de detectar en JS.
* SWC:
Es un transpilador, que convierte JavaScript a JSX. Es mucho más rápido que otras alternativas como Babel, ya que está hecho en Rust

Versión de vite: vite v7.3.1
Vite es el empaquetador más rápido para crear aplicaciones web.

El proyecto tiene la siguiente estructura de archivos y carpetas:
- node_modules: carpeta donde se importan las librerías o paquetes externos de los que depende el proyecto para funcionar. No se conserva en el repositorio si no que se crea al instalar las dependencias en 
- public:
- src: el código propio del proyecto. Componentes basados en react, recursos como imagenes, etc.
  - assets:
  - App.css: Estilos css del componente App base de la aplicaion react
  - App.tsx: Codigo JSX (TypeScript Extendido) del componente base de la aplicación web: App. Este componente es importado y untilizado en main.tsx, y es el componete que contiene o invoca a toda al jerarquia de componentes utilizados en la aplicacion web.
  - index.css: Estilo base de la aplicacion. Los estilos pueden ser sobreescritos por los de los componentes. Generalmente utilizado para dar estilo general a etiquetas html basicas como body, etc.
  - main.tsx: Es importado desde el index.html y a su vez instancia el componente App y lo inserta ya renderizado en el elemento html con id "root".
- .gitignore: se nombran archivos y rutas dentro del proyecto que no es necesario respaldar en el repositorio, como las dependencias instaladas en node_modules. O también deben listarse archivos que contengan información sensible, como .env
- eslint.config.js:


# Readme made by Vite:

# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is currently not compatible with SWC. See [this issue](https://github.com/vitejs/vite-plugin-react/issues/428) for tracking the progress.

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
