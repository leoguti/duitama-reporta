# Seguridad Ciudadana - Nadia

## Tu misión
Crear una página web donde los ciudadanos de Duitama puedan reportar problemas de seguridad en calles y transporte público, y que se vean en un mapa.

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
- Un título que diga "Seguridad Ciudadana - Duitama"
- Un mapa de OpenStreetMap centrado en Duitama, Colombia (latitud 5.8268, longitud -73.0333) usando la librería Leaflet
- El mapa debe ocupar la mitad de la pantalla
- Debajo del mapa un formulario con estos campos: tipo de incidente (robo, acoso, pelea, zona oscura, otro), hora aproximada (mañana, tarde, noche, madrugada), descripción, y un botón de enviar
- Usa colores azul oscuro como de seguridad y protección
- Incluye los CDN de Leaflet en el HTML
```

**Mensaje 2 - Hacer clic en el mapa para marcar ubicación:**
```
Modifica el código para que cuando el usuario haga clic en el mapa se ponga un marcador en ese punto y se guarden las coordenadas. Si hace clic en otro lado el marcador se mueve. Muestra las coordenadas debajo del mapa en un texto que diga "Ubicación del incidente: lat, lng"
```

**Mensaje 3 - Mostrar los reportes como tarjetas:**
```
Agrega que cuando se presione el botón de enviar, se cree una tarjeta debajo del formulario con la información del reporte (tipo de incidente, hora, descripción, coordenadas) y se agregue un marcador permanente en el mapa con un popup que muestre el tipo de incidente y la hora. Los reportes se guardan en una lista en JavaScript. Limpia el formulario después de enviar.
```

**Mensaje 4 - Marcadores con iconos según tipo:**
```
Cambia los marcadores del mapa para que tengan colores diferentes según el tipo de incidente: rojo para robo, naranja para acoso, amarillo para pelea, morado para zona oscura, gris para otro. Usa círculos de colores.
```

**Mensaje 5 - Mapa de calor de zonas peligrosas:**
```
Agrega un botón que diga "Ver zonas de riesgo" que al presionarlo muestre los reportes agrupados por zona, resaltando con un círculo grande semitransparente rojo las zonas donde hay más reportes concentrados. Otro botón "Ver marcadores" para volver a la vista normal.
```

### Paso 3 - Sube tu código
1. Ve a tu carpeta `nadia/` en el repo `duitama-reporta`
2. Crea un archivo `index.html`
3. Pega todo el código que generó Copilot
4. Haz commit

### Paso 4 - Verifica
Abre tu página en GitHub Pages y revisa que funcione el mapa, el formulario y los colores según tipo de incidente.
