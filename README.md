# Hoja de conteo de stock técnico

Hoja en blanco para que cualquier técnico cuente su material. Mismas 120 referencias del catálogo, todas a cero.

## Qué hace

- Al abrirla pide **nombre y apellidos** y **matrícula**. Sin los dos no se entra a la lista.
- Cuatro pestañas por tipo de cantidad: Propio, Tránsito, Defectuoso y Stock type.
- Botones − y + por referencia, o tocar el número para escribirlo.
- Las referencias sin tocar salen en gris; al contarlas se marcan y avanza la barra de progreso (X/120).
- Filtros: todas, sin contar, contadas, con unidades. Y buscador por referencia o descripción.
- **Copiar resumen**: texto con nombre, matrícula, fecha y solo las referencias con unidades, para pegar en WhatsApp o correo.
- **Guardar CSV**: descarga `conteo-<matrícula>-<fecha>.csv` con las 120 referencias y las cantidades.

## Datos

El conteo se guarda en el `localStorage` del navegador del técnico. Cada uno ve solo el suyo y no se sincroniza con nadie: lo que llega de vuelta es el CSV o el resumen que envíe.

Si se cierra y se vuelve a abrir, recupera lo contado y la identificación. **Vaciar** pone la hoja a cero otra vez.

## Publicar en GitHub Pages

1. Sube estos ficheros a la raíz del repositorio.
2. Settings → Pages → Source: *Deploy from a branch*, rama `main`, carpeta `/ (root)`.
3. Pasa el enlace `https://<usuario>.github.io/<repositorio>/` a los técnicos.

Desde el móvil, "Añadir a pantalla de inicio" la instala como app y funciona sin cobertura, que es lo normal contando en un trastero o en la furgoneta.

## Cambiar el catálogo

Las referencias están en la constante `BASE` de `index.html`, en el formato `["referencia", "descripción"]`. Añadir o quitar líneas es todo lo que hace falta.
