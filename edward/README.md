# Seguridad en los Barrios - Edward

## Tu misión
Crear una página web donde vecinos de tu barrio puedan reportar problemas de seguridad como venta de drogas, consumo en espacios públicos y otros problemas, y que se vean en un mapa.

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
- Un título que diga "Seguridad Barrial - Duitama"
- Un mapa de OpenStreetMap centrado en Duitama, Colombia (latitud 5.8268, longitud -73.0333) usando la librería Leaflet
- El mapa debe ocupar la mitad de la pantalla
- Debajo del mapa un formulario con estos campos: tipo de problema (venta de drogas, consumo en vía pública, vandalismo, falta de iluminación, otro), frecuencia (una vez, frecuente, permanente), descripción, y un botón de enviar
- Usa colores oscuros, negro y rojo, que den sensación de alerta
- Incluye los CDN de Leaflet en el HTML
```

**Mensaje 2 - Hacer clic en el mapa para marcar ubicación:**
```
Modifica el código para que cuando el usuario haga clic en el mapa se ponga un marcador en ese punto y se guarden las coordenadas. Si hace clic en otro lado el marcador se mueve. Muestra las coordenadas debajo del mapa en un texto que diga "Ubicación del reporte: lat, lng"
```

**Mensaje 3 - Mostrar los reportes como tarjetas:**
```
Agrega que cuando se presione el botón de enviar, se cree una tarjeta debajo del formulario con la información del reporte (tipo, frecuencia, descripción, coordenadas) y se agregue un marcador permanente en el mapa con un popup que muestre el tipo y la frecuencia. Los reportes se guardan en una lista en JavaScript. Limpia el formulario después de enviar.
```

**Mensaje 4 - Marcadores con colores según frecuencia:**
```
Cambia los marcadores del mapa para que tengan colores diferentes según la frecuencia: amarillo para una vez, naranja para frecuente, rojo para permanente. Usa círculos de colores. Los permanentes deben verse más grandes que los de una vez.
```

**Mensaje 5 - Reporte anónimo y contador:**
```
Agrega un checkbox que diga "Reportar de forma anónima" que esté marcado por defecto. Agrega arriba del mapa un panel que muestre: total de reportes, el tipo de problema más reportado, y cuántos son permanentes. Que se actualice automáticamente.
```

### Paso 3 - Sube tu código
1. Ve a tu carpeta `edward/` en el repo `duitama-reporta`
2. Crea un archivo `index.html`
3. Pega todo el código que generó Copilot
4. Haz commit

### Paso 4 - Verifica
Abre tu página en GitHub Pages y revisa que funcione el mapa, el formulario y que los colores cambien según la frecuencia.
