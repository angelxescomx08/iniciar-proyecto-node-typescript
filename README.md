# Pasos para iniciar un proyecto de node con typescript

## 1. Inicializar el package.json

La forma más rápida de crear un package.json es con el comando:

```
npm init -y
```

## 2. Instalar typescript

Para instalar typescript se debe recordar que esta debe ser una dependencia de desarrollo. Para instalar typescript usamos el comando:

```
npm i typescript -D
```

## 3. Inicializar typescript

Debemos de hacer cambios en los scripts de nuestro package.json, un comando útil es **tsc**:

```json
"scripts": {
  "tsc": "tsc",
  "test": "echo \"Error: no test specified\" && exit 1"
},
```

Ahora que ya configuramos el script podemos usarlo con npm, notar que se pone el "--" para que el "--init" le llegue como argumento al "tsc" en lugar del "npm":

```
npm run tsc -- --init
```

Todo esto generará el archivo **tsconfig.json** que usaremos para configurar typescript.

## 4. Configurar typescript

La configuración es a tu criterio, sin embargo una configuración recomendada es la salida del output de typescript. Recomiendo que apunte a una carpeta de build:

```json
{
  "outDir": "./build"
}
```