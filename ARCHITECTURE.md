# Arquitectura del Proyecto

El proyecto tiene la siguiente estructura de archivos y carpetas:

```
📁 proyecto/
├── 📁 node_modules/
├── 📁 public/
├── 📁 src/
│   ├── 📁 assets/
│   ├── 📄 App.css
│   ├── 📄 App.tsx
│   ├── 📄 index.css
│   └── 📄 main.tsx
├── 📄 .gitignore
└── 📄 eslint.config.js
```

## Descripción de carpetas y archivos

### `node_modules/`
Carpeta donde se importan las librerías o paquetes externos de los que depende el proyecto para funcionar. No se conserva en el repositorio si no que se crea al instalar las dependencias en

### `public/`

### `src/`
El código propio del proyecto. Componentes basados en react, recursos como imagenes, etc.

#### `assets/`

#### `App.css`
Estilos css del componente App base de la aplicaion react

#### `App.tsx`
Codigo JSX (TypeScript Extendido) del componente base de la aplicación web: App. Este componente es importado y untilizado en main.tsx, y es el componete que contiene o invoca a toda al jerarquia de componentes utilizados en la aplicacion web.

#### `index.css`
Estilo base de la aplicacion. Los estilos pueden ser sobreescritos por los de los componentes. Generalmente utilizado para dar estilo general a etiquetas html basicas como body, etc.

#### `main.tsx`
Es importado desde el index.html y a su vez instancia el componente App y lo inserta ya renderizado en el elemento html con id "root".

### `.gitignore`
Se nombran archivos y rutas dentro del proyecto que no es necesario respaldar en el repositorio, como las dependencias instaladas en node_modules. O también deben listarse archivos que contengan información sensible, como .env

### `eslint.config.js`