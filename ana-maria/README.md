# Cruces Férreos Peligrosos - Ana María

## Tu misión
Crear una página web con un mapa que muestre todos los cruces donde la vía del tren atraviesa calles en Duitama, documentando el estado de cada cruce, si tiene señalización, y si ha habido accidentes.

## Instrucciones

### Paso 1 - Abre GitHub Copilot
1. Ve a **github.com/copilot** en tu navegador
2. Si no lo tienes activado, ve a **github.com/settings/copilot** y actívalo (es gratis)

### Paso 2 - Usa estos 5 mensajes (uno por uno)
Copia cada mensaje, pégalo en el chat de Copilot, y guarda el código que te dé en un archivo `index.html` en esta carpeta.

---

**Mensaje 1 - La página base con mapa:**
```
Hazme una página web en HTML con CSS y JavaScript que tenga:
- Un título que diga "Cruces Férreos Peligrosos - Duitama"
- Un subtítulo que diga "La vía del tren divide nuestra ciudad. Estos son los cruces que necesitan atención."
- Un mapa de OpenStreetMap centrado en Duitama, Colombia (latitud 5.8268, longitud -73.0333) usando la librería Leaflet con zoom 14
- El mapa debe ocupar la mitad de la pantalla
- Debajo del mapa un formulario con estos campos: nombre del cruce o calle, tiene señalización (sí, no, dañada), tiene barrera (sí, no, dañada), nivel de riesgo (bajo, medio, alto, crítico), ha habido accidentes (sí, no, no sé), descripción, y un botón de enviar
- Usa colores amarillo y negro como las señales de precaución de trenes
- Incluye los CDN de Leaflet en el HTML
```

**Mensaje 2 - Hacer clic en el mapa para marcar ubicación:**
```
Modifica el código para que cuando el usuario haga clic en el mapa se ponga un marcador en ese punto y se guarden las coordenadas. Si hace clic en otro lado el marcador se mueve. Muestra las coordenadas debajo del mapa en un texto que diga "Ubicación del cruce: lat, lng"
```

**Mensaje 3 - Mostrar los cruces como tarjetas:**
```
Agrega que cuando se presione el botón de enviar, se cree una tarjeta debajo del formulario con toda la información del cruce (nombre, señalización, barrera, riesgo, accidentes, descripción) y se agregue un marcador permanente en el mapa con un popup detallado. Los cruces se guardan en una lista en JavaScript. Limpia el formulario después de enviar.
```

**Mensaje 4 - Marcadores con colores según nivel de riesgo:**
```
Cambia los marcadores del mapa para que tengan colores diferentes según el nivel de riesgo: verde para bajo, amarillo para medio, naranja para alto, rojo para crítico. Los que tienen accidentes reportados deben tener un borde negro grueso. Usa círculos de colores.
```

**Mensaje 5 - Resumen de hallazgos:**
```
Agrega arriba del mapa un panel de resumen que muestre: total de cruces registrados, cuántos son de riesgo alto o crítico, cuántos NO tienen señalización, cuántos NO tienen barrera, y cuántos tienen accidentes reportados. Agrega un mensaje de alerta en rojo si hay cruces críticos sin señalización.
```

### Paso 3 - Sube tu código
1. Ve al repo **duitama-reporta** en GitHub: https://github.com/leoguti/duitama-reporta
2. Primero acepta la invitación si no lo has hecho (te aparece un banner amarillo arriba)
3. Entra a tu carpeta
4. Haz clic en **Add file** → **Create new file**
5. En el nombre del archivo escribe: `index.html`
6. Pega todo el código que generó Copilot
7. Abajo haz clic en el botón verde **Commit changes**

### Paso 4 - Ver tu página en internet
Tu página ya está publicada en GitHub Pages. Para verla:

1. Ve a: **https://leoguti.github.io/duitama-reporta/TU-CARPETA/**
2. Si no carga, espera 1-2 minutos y recarga la página (F5)
3. Si sale error 404, revisa que tu archivo se llame exactamente `index.html` (todo en minúsculas)

**Tu link directo es:**
https://leoguti.github.io/duitama-reporta/ana-maria/

### Paso 5 - Verifica
Abre tu link y revisa que funcione el mapa, el formulario y que los colores reflejen el nivel de riesgo de cada cruce.
