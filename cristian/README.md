# Reporte de Basuras y Canecas - Cristian

## Tu misión
Crear una página web donde cualquier persona pueda reportar puntos de basura acumulada en Duitama y ver en un mapa dónde están las canecas y dónde hacen falta.

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
- Un título que diga "Reporte de Basuras - Duitama"
- Un mapa de OpenStreetMap centrado en Duitama, Colombia (latitud 5.8268, longitud -73.0333) usando la librería Leaflet
- El mapa debe ocupar la mitad de la pantalla
- Debajo del mapa un formulario con estos campos: tipo de problema (basura acumulada, caneca dañada, falta caneca), descripción del problema, y un botón de enviar
- Usa colores verdes porque es tema ambiental
- Incluye los CDN de Leaflet en el HTML
```

**Mensaje 2 - Hacer clic en el mapa para marcar ubicación:**
```
Modifica el código para que cuando el usuario haga clic en el mapa se ponga un marcador en ese punto y se guarden las coordenadas. Si hace clic en otro lado el marcador se mueve. Muestra las coordenadas debajo del mapa en un texto que diga "Ubicación seleccionada: lat, lng"
```

**Mensaje 3 - Mostrar los reportes como tarjetas:**
```
Agrega que cuando se presione el botón de enviar, se cree una tarjeta debajo del formulario con la información del reporte (tipo, descripción, coordenadas) y se agregue un marcador permanente en el mapa con un popup que muestre el tipo de problema. Los reportes se guardan en una lista en JavaScript. Limpia el formulario después de enviar.
```

**Mensaje 4 - Marcadores con colores según tipo:**
```
Cambia los marcadores del mapa para que tengan colores diferentes según el tipo de problema: rojo para basura acumulada, naranja para caneca dañada, azul para falta caneca. Usa iconos de Leaflet con colores o círculos de colores.
```

**Mensaje 5 - Filtro por tipo de problema:**
```
Agrega arriba del mapa tres botones para filtrar los reportes por tipo: "Basura acumulada", "Caneca dañada", "Falta caneca" y un botón "Todos". Al hacer clic en un botón solo se muestran los marcadores y tarjetas de ese tipo.
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
https://leoguti.github.io/duitama-reporta/cristian/

### Paso 5 - Verifica
Abre tu link y revisa que funcione el mapa, el formulario y los marcadores.
