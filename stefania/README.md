# Reportes de la Calle - Stefania

## Tu misión
Crear una página web donde cualquier persona pueda reportar problemas que vea en las calles de Duitama: semáforos dañados, señales caídas, andenes rotos, postes de luz apagados, y cualquier otro problema que afecte a los peatones y conductores.

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
- Un título que diga "Reportes de la Calle - Duitama"
- Un mapa de OpenStreetMap centrado en Duitama, Colombia (latitud 5.8268, longitud -73.0333) usando la librería Leaflet
- El mapa debe ocupar la mitad de la pantalla
- Debajo del mapa un formulario con estos campos: tipo de problema (semáforo dañado, señal caída, andén roto, poste de luz apagado, alcantarilla sin tapa, otro), qué tan urgente es (poco urgente, urgente, muy urgente), descripción, y un botón de enviar
- Usa colores celeste y blanco como el cielo de la ciudad
- Incluye los CDN de Leaflet en el HTML
```

**Mensaje 2 - Hacer clic en el mapa para marcar ubicación:**
```
Modifica el código para que cuando el usuario haga clic en el mapa se ponga un marcador en ese punto y se guarden las coordenadas. Si hace clic en otro lado el marcador se mueve. Muestra las coordenadas debajo del mapa en un texto que diga "Ubicación del problema: lat, lng"
```

**Mensaje 3 - Mostrar los reportes como tarjetas:**
```
Agrega que cuando se presione el botón de enviar, se cree una tarjeta debajo del formulario con la información del reporte (tipo, urgencia, descripción, coordenadas) y se agregue un marcador permanente en el mapa con un popup que muestre el tipo y la urgencia. Los reportes se guardan en una lista en JavaScript. Limpia el formulario después de enviar.
```

**Mensaje 4 - Marcadores con colores según urgencia:**
```
Cambia los marcadores del mapa para que tengan colores diferentes según la urgencia: verde para poco urgente, amarillo para urgente, rojo para muy urgente. Usa círculos de colores. Los muy urgentes deben ser más grandes.
```

**Mensaje 5 - Lista de problemas ordenada por urgencia:**
```
Agrega un botón que diga "Ver más urgentes primero" que ordene las tarjetas de reportes de más urgente a menos urgente. Agrega otro botón "Ver más recientes primero" que los ordene por orden en que se agregaron. Muestra un contador arriba que diga cuántos reportes hay en total.
```

### Paso 3 - Sube tu código
1. Ve a tu carpeta `stefania/` en el repo `duitama-reporta`
2. Crea un archivo `index.html`
3. Pega todo el código que generó Copilot
4. Haz commit

### Paso 4 - Verifica
Abre tu página en GitHub Pages y revisa que funcione el mapa, el formulario y que los colores cambien según la urgencia.
