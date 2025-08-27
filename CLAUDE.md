# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Comandos de desarrollo

1. `npm run dev` - Inicia el servidor de desarrollo con Vite
2. `npm run build` - Compila TypeScript y construye para producción
3. `npm run preview` - Vista previa de la construcción de producción

## Arquitectura del proyecto

### Estructura general
- **Proyecto de refuerzo**: TypeScript con Vite para aprender conceptos básicos de TS/JS
- **Carpeta `src/bases/`**: Contiene ejercicios numerados (01-11) que cubren conceptos fundamentales
- **Carpeta `src/data/`**: Datos de ejemplo (héroes) y tipos/interfaces compartidos

### Sistema de ejercicios
- Los archivos en `bases/` siguen nomenclatura numérica: `01-const-let.ts`, `02-template-string.ts`, etc.
- `main.ts` importa selectivamente ejercicios específicos (comentar/descomentar para probar diferentes ejercicios)
- Los ejercicios cubren: variables, template strings, objetos, arrays, funciones, destructuring, import/export, promesas, fetch, async/await

### Patrones importantes
- **Tipos e interfaces**: Definidos en `data/heroes.data.ts` con enum `Owner` para DC/Marvel
- **Funciones exportadas**: Ejemplo en `08-imp-exp.ts` con `getHeroesByOwner()` que filtra héroes por propietario
- **Documentación JSDoc**: Se usa para funciones principales con ejemplos de parámetros y retornos

### Configuración TypeScript
- Modo estricto habilitado con verificaciones adicionales (`noUnusedLocals`, `noUnusedParameters`)
- Target ES2020 con resolución de módulos "bundler"
- Solo incluye archivos del directorio `src/`

### Notas de desarrollo
- Para probar un ejercicio específico, descomenta su import en `main.ts`
- Los console.log están comentados en los ejercicios - descomentarlos para ver resultados
- El proyecto usa Vite como bundler y servidor de desarrollo