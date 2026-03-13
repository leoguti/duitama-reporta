# Reporte de Huecos en las Vías - Yosef

## Tu misión
Crear una página web donde cualquier persona pueda reportar huecos y problemas en las vías de Duitama y verlos en un mapa.

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
- Un título que diga "Huecos en las Vías - Duitama"
- Un mapa de OpenStreetMap centrado en Duitama, Colombia (latitud 5.8268, longitud -73.0333) usando la librería Leaflet
- El mapa debe ocupar la mitad de la pantalla
- Debajo del mapa un formulario con estos campos: gravedad del hueco (leve, grave, peligroso), tamaño aproximado (pequeño, mediano, grande), descripción, y un botón de enviar
- Usa colores naranjas y grises como de construcción y carreteras
- Incluye los CDN de Leaflet en el HTML
```

**Mensaje 2 - Hacer clic en el mapa para marcar ubicación:**
```
Modifica el código para que cuando el usuario haga clic en el mapa se ponga un marcador en ese punto y se guarden las coordenadas. Si hace clic en otro lado el marcador se mueve. Muestra las coordenadas debajo del mapa en un texto que diga "Ubicación seleccionada: lat, lng"
```

**Mensaje 3 - Mostrar los reportes como tarjetas:**
```
Agrega que cuando se presione el botón de enviar, se cree una tarjeta debajo del formulario con la información del reporte (gravedad, tamaño, descripción, coordenadas) y se agregue un marcador permanente en el mapa con un popup que muestre la gravedad y el tamaño. Los reportes se guardan en una lista en JavaScript. Limpia el formulario después de enviar.
```

**Mensaje 4 - Marcadores con colores según gravedad:**
```
Cambia los marcadores del mapa para que tengan colores diferentes según la gravedad: amarillo para leve, naranja para grave, rojo para peligroso. Usa círculos de colores en el mapa. Que el tamaño del círculo cambie según el tamaño del hueco: pequeño 10px, mediano 20px, grande 30px.
```

**Mensaje 5 - Contador de reportes:**
```
Agrega arriba del mapa un panel con estadísticas: total de reportes, cuántos son leves, cuántos graves, cuántos peligrosos. Que se actualice cada vez que se agrega un reporte nuevo.
```

### Paso 3 - Sube tu código
1. Ve a tu carpeta `yosef/` en el repo `duitama-reporta`
2. Crea un archivo `index.html`
3. Pega todo el código que generó Copilot
4. Haz commit

### Paso 4 - Verifica
Abre tu página en GitHub Pages y revisa que funcione el mapa, el formulario y los marcadores con colores.
