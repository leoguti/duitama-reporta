// ==============================
// CREAR MAPA
// ==============================

var map = L.map('map').setView([5.8268, -73.0333], 14);

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',{
maxZoom:19,
attribution:'© OpenStreetMap'
}).addTo(map);


// ==============================
// VARIABLES
// ==============================

let marcadorTemporal = null;
let cruces = [];


// ==============================
// COLORES SEGÚN RIESGO
// ==============================

function colorRiesgo(riesgo){

switch(riesgo){

case "bajo":
return "green";

case "medio":
return "yellow";

case "alto":
return "orange";

case "crítico":
return "red";

default:
return "gray";

}

}


// ==============================
// CLICK EN MAPA
// ==============================

map.on("click",function(e){

let lat = e.latlng.lat.toFixed(6);
let lng = e.latlng.lng.toFixed(6);

if(marcadorTemporal == null){

marcadorTemporal = L.marker([lat,lng]).addTo(map);

}else{

marcadorTemporal.setLatLng([lat,lng]);

}

document.getElementById("coords").innerText =
"Ubicación del cruce: " + lat + ", " + lng;

document.getElementById("lat").value = lat;
document.getElementById("lng").value = lng;

});



// ==============================
// ACTUALIZAR PANEL DE RESUMEN
// ==============================

function actualizarPanel(){

let total = cruces.length;

let riesgoAlto = 0;
let sinSenal = 0;
let sinBarrera = 0;
let conAccidentes = 0;

let alertaCritica = false;

cruces.forEach(c => {

if(c.riesgo === "alto" || c.riesgo === "crítico"){
riesgoAlto++;
}

if(c.senalizacion === "no"){
sinSenal++;
}

if(c.barrera === "no"){
sinBarrera++;
}

if(c.accidentes === "sí"){
conAccidentes++;
}

if(c.riesgo === "crítico" && c.senalizacion === "no"){
alertaCritica = true;
}

});

document.getElementById("totalCruces").innerText = total;
document.getElementById("riesgoAlto").innerText = riesgoAlto;
document.getElementById("sinSenal").innerText = sinSenal;
document.getElementById("sinBarrera").innerText = sinBarrera;
document.getElementById("conAccidentes").innerText = conAccidentes;

let alerta = document.getElementById("alertaCritica");

if(alertaCritica){

alerta.style.display = "block";
alerta.innerText = "⚠ ALERTA: Existe al menos un cruce CRÍTICO sin señalización";

}else{

alerta.style.display = "none";

}

}



// ==============================
// FORMULARIO
// ==============================

document.getElementById("formCruce").addEventListener("submit",function(e){

e.preventDefault();

let lat = document.getElementById("lat").value;
let lng = document.getElementById("lng").value;

if(!lat){

alert("Selecciona primero la ubicación en el mapa");

return;

}

let cruce = {

nombre:document.getElementById("nombre").value,
senalizacion:document.getElementById("senalizacion").value,
barrera:document.getElementById("barrera").value,
riesgo:document.getElementById("riesgo").value,
accidentes:document.getElementById("accidentes").value,
descripcion:document.getElementById("descripcion").value,
lat:lat,
lng:lng

};

cruces.push(cruce);


// ==============================
// CREAR TARJETA
// ==============================

let tarjeta = document.createElement("div");

tarjeta.className = "tarjeta";

tarjeta.innerHTML = `

<h3>${cruce.nombre}</h3>

<p><b>Señalización:</b> ${cruce.senalizacion}</p>

<p><b>Barrera:</b> ${cruce.barrera}</p>

<p><b>Riesgo:</b> ${cruce.riesgo}</p>

<p><b>Accidentes:</b> ${cruce.accidentes}</p>

<p>${cruce.descripcion}</p>

<p><b>Coordenadas:</b> ${cruce.lat}, ${cruce.lng}</p>

`;

document.getElementById("listaCruces").appendChild(tarjeta);


// ==============================
// CREAR MARCADOR
// ==============================

let color = colorRiesgo(cruce.riesgo);

let borde = cruce.accidentes === "sí" ? "black" : "#333";

let grosor = cruce.accidentes === "sí" ? 4 : 1;

let marcador = L.circleMarker([cruce.lat, cruce.lng],{

radius:10,
fillColor:color,
color:borde,
weight:grosor,
fillOpacity:0.9

}).addTo(map);

marcador.bindPopup(`

<b>${cruce.nombre}</b><br>

Señalización: ${cruce.senalizacion}<br>

Barrera: ${cruce.barrera}<br>

Riesgo: ${cruce.riesgo}<br>

Accidentes: ${cruce.accidentes}<br>

${cruce.descripcion}

`);


// ==============================
// LIMPIAR FORMULARIO
// ==============================

if(marcadorTemporal){

map.removeLayer(marcadorTemporal);

marcadorTemporal = null;

}

document.getElementById("formCruce").reset();

document.getElementById("coords").innerText =
"Ubicación del cruce: Haz clic en el mapa";

document.getElementById("lat").value = "";
document.getElementById("lng").value = "";


// ACTUALIZAR PANEL

actualizarPanel();

});



// ==============================
// CARGAR VIA FERREA (OSM)
// ==============================

const railwayQuery = `
[out:json][timeout:25];
(
way["railway"="rail"](5.78,-73.08,5.87,-72.98);
);
out geom;
`;

fetch("https://overpass-api.de/api/interpreter", {

method:"POST",
body:railwayQuery

})
.then(res => res.json())
.then(data => {

data.elements.forEach(el => {

if(el.type === "way"){

let coords = el.geometry.map(p => [p.lat, p.lon]);

L.polyline(coords,{

color:"purple",
weight:5,
opacity:0.9

}).addTo(map)
.bindPopup("Vía férrea");

}

});

});



// ==============================
// CARGAR CRUCES REALES OSM
// ==============================

const crossingQuery = `
[out:json][timeout:25];
(
node["railway"="level_crossing"](5.78,-73.08,5.87,-72.98);
node["railway"="crossing"](5.78,-73.08,5.87,-72.98);
);
out;
`;

fetch("https://overpass-api.de/api/interpreter", {

method:"POST",
body:crossingQuery

})
.then(res => res.json())
.then(data => {

data.elements.forEach(node => {

L.circleMarker([node.lat, node.lon],{

radius:6,
fillColor:"#000",
color:"#fff",
weight:2,
fillOpacity:1

})
.addTo(map)
.bindPopup("Cruce ferroviario registrado en OpenStreetMap");

});

});
