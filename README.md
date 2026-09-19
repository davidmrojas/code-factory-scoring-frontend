# Motor de Riesgo Crediticio

Interfaz web para el registro de solicitantes y la captura de información financiera inicial de un motor de scoring de riesgo crediticio.

El proyecto corresponde al Sprint 1 de Análisis y Diseño de Sistemas I y está construido con React, TypeScript, Vite y Tailwind CSS.

## Requisitos

- Node.js 22 o superior
- pnpm 12 o superior

## Instalación

```bash
pnpm install
```

## Desarrollo

```bash
pnpm dev
```

La aplicación estará disponible en `http://localhost:8443`.

## Validación y producción

```bash
pnpm exec tsc --noEmit
pnpm build
pnpm preview
```

`pnpm build` genera la aplicación optimizada en `dist/`.

## Funcionalidades del Sprint 1

- Registro básico con tipo y número de documento, nombres, apellidos, correo y teléfono.
- Validación de campos obligatorios, correo electrónico y teléfono numérico.
- Detección simulada de documentos duplicados.
- Registro y validación de ingresos mensuales y egresos fijos.
- Cálculo en tiempo real del ingreso neto disponible.
- Resumen financiero consolidado con estado visual positivo o negativo.
- Notificaciones de confirmación y errores de operación.
- Controles accesibles con etiquetas asociadas, estados ARIA y mensajes descriptivos.

## Estructura principal

```text
src/
  App.tsx       Flujo principal, componentes y reglas del Sprint 1
  index.css     Importación de Tailwind y fuentes globales
  main.tsx      Punto de entrada de React
public/assets/  Iconos estáticos de la interfaz
index.html      Documento HTML base
vite.config.ts  Configuración de Vite, React y Tailwind
```

## Integración con backend

Las funciones de persistencia están preparadas como operaciones asíncronas simuladas. El mock de duplicados se encuentra en `checkDuplicate` y puede sustituirse por una llamada `fetch` hacia el servicio REST correspondiente sin cambiar el flujo de la interfaz.

## Convenciones

- TypeScript en modo estricto.
- Componentes y funciones con nombres descriptivos en español, sin caracteres especiales en identificadores.
- Clases utilitarias de Tailwind para los estilos de la interfaz.
- Archivos generados y dependencias excluidos mediante `.gitignore`.
