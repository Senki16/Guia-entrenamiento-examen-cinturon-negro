# Guía de Entrenamiento · Examen de Cinturón Negro de Taekwondo

Página web con la guía completa de preparación: básicos, patrones, taegeuks (con
video de referencia), teoría, combate y defensa personal.

El camino a maestro de taekwondo 🥋

## Estructura del proyecto

```
.
├── index.html        ← la página web (se abre sola en Vercel)
├── vercel.json       ← configuración para servir el video correctamente
├── .gitattributes    ← configuración de Git LFS para el video
└── video/
    └── taegeuk-poomsae-1-8.mp4   ← AQUÍ debes colocar tu video
```

## Paso 1 · Coloca el video

Renombra tu archivo descargado
("All Taegeuk Poomsae 태극 품새 전체 1-8장") a:

```
taegeuk-poomsae-1-8.mp4
```

y colócalo dentro de la carpeta `video/`. El nombre debe ir en minúsculas,
sin espacios ni acentos, o el navegador no lo encontrará.

## Paso 2 · Sube todo a GitHub

### Si el video pesa MENOS de 100 MB

```bash
git clone https://github.com/Senki16/Guia-entrenamiento-examen-cinturon-negro.git
cd Guia-entrenamiento-examen-cinturon-negro
# copia aquí index.html, vercel.json, .gitattributes y la carpeta video/
git add .
git commit -m "Guía de entrenamiento + video de taegeuks"
git push origin main
```

### Si el video pesa MÁS de 100 MB (lo más probable)

GitHub rechaza archivos de más de 100 MB. Usa Git LFS (incluido el
.gitattributes ya está configurado):

```bash
# instala Git LFS una sola vez: https://git-lfs.com
git lfs install
git clone https://github.com/Senki16/Guia-entrenamiento-examen-cinturon-negro.git
cd Guia-entrenamiento-examen-cinturon-negro
# copia aquí todos los archivos incluyendo video/taegeuk-poomsae-1-8.mp4
git lfs track "*.mp4"
git add .gitattributes
git add .
git commit -m "Guía de entrenamiento + video de taegeuks (LFS)"
git push origin main
```

> Nota: Git LFS gratuito tiene 1 GB de almacenamiento y 1 GB de ancho de banda
> al mes. Si el video es muy pesado, considera comprimirlo (por ejemplo con
> HandBrake) a menos de 100 MB para evitar LFS por completo.

## Paso 3 · Despliega en Vercel

1. Entra a https://vercel.com e inicia sesión con tu cuenta de GitHub.
2. "Add New… → Project" y selecciona este repositorio.
3. No cambies nada (no necesita build). Pulsa "Deploy".
4. Vercel te dará una URL pública con tu guía funcionando.

¡Listo! 화이팅!
