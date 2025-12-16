# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).# ⚡ Falquito Stack App

Este proyecto fue generado automáticamente usando **[create-falquito-stack](https://www.npmjs.com/package/create-falquito-stack)**.
Es un entorno de desarrollo robusto, tipado y pre-configurado para escalar.

## 🛠️ Stack Tecnológico

Todo lo que necesitas para construir una UI moderna ya está instalado y configurado:

| Herramienta | Propósito | Documentación |
| :--- | :--- | :--- |
| **⚛️ React + Vite** | Framework y Bundler ultra-rápido. | [Vite Docs](https://vitejs.dev/) |
| **📘 TypeScript** | Seguridad de tipos estática. | [TS Docs](https://www.typescriptlang.org/) |
| **🛣️ React Router** | Enrutamiento del lado del cliente. | [React Router](https://reactrouter.com/) |
| **⚡ TanStack Query** | Gestión de estado asíncrono y caché. | [TanStack Query](https://tanstack.com/query/latest) |
| **📊 TanStack Table** | Tablas headless para datos complejos. | [TanStack Table](https://tanstack.com/table/latest) |
| **🎨 TailwindCSS** | Estilizado con clases de utilidad. | [Tailwind Docs](https://tailwindcss.com/) |
| **💎 Ant Design** | Set de componentes UI listos para usar. | [Ant Design](https://ant.design/) |

---

## 🚀 Comandos Disponibles

En la terminal del proyecto puedes ejecutar:

### `npm run dev`
Inicia el servidor de desarrollo en modo local (con Hot Module Replacement).

### `npm run build`
Compila la aplicación para producción en la carpeta `dist`.

### `npm run lint`
Ejecuta ESLint para encontrar errores en el código.

### `npm run preview`
Sirve localmente la versión de producción construida (útil para probar antes de desplegar).

---

## 📂 Estructura del Proyecto

```text
src/
├── assets/       
├── components/   
├── handlers/    
├── pages/        
├── layouts/    
├── stores/       
├── utils/        
└── App.tsx       

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
