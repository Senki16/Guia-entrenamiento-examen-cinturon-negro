# Instrucciones para actualizar GitHub

Sigue estos pasos desde tu computadora para subir los archivos actualizados al repositorio:

## Paso 1: Clonar o navegar al repositorio

Si aún no lo tienes clonado:
```bash
git clone https://github.com/Senki16/Guia-entrenamiento-examen-cinturon-negro.git
cd Guia-entrenamiento-examen-cinturon-negro
```

Si ya lo tienes, solo navega a la carpeta:
```bash
cd Guia-entrenamiento-examen-cinturon-negro
```

## Paso 2: Reemplazar los archivos

Copia estos archivos **desde la carpeta `files-github/` que descargaste** hacia la raíz de tu repositorio local:

- `index.html` → reemplaza el archivo existente
- `vercel.json` → ya está ahí, solo reemplaza
- `assets/` → copia toda la carpeta (crea una nueva si no existe)

La estructura debe quedar así:
```
Guia-entrenamiento-examen-cinturon-negro/
├── index.html             ← archivo nuevo
├── vercel.json            ← mantener
├── README.md              ← mantener (ya existe)
├── assets/                ← carpeta nueva
│   ├── banner.png
│   ├── flyer.png
│   ├── historia_club.png
│   ├── logo.png
│   ├── master_award.png
│   ├── master_cert.png
│   └── master_gold.png
└── video/                 ← mantener (ya existe, opcional)
    └── taegeuk-poomsae-1-8.mp4
```

## Paso 3: Verificar cambios

```bash
git status
```

Verás que:
- `index.html` está modificado
- `assets/` es una carpeta nueva con 7 imágenes

## Paso 4: Commit y Push

```bash
# Añadir todos los cambios
git add -A

# Hacer commit con descripción
git commit -m "Actualización: Sitio oficial Club Taekwondo Dragón Rojo con nuevas secciones, assets e iframe de YouTube actualizado"

# Subir a GitHub
git push origin main
```

## ¿Listo?

Tu repositorio estará actualizado en GitHub. Vercel detectará los cambios automáticamente y desplegará la nueva versión.

---

## Resumen de cambios

✅ **Nuevo `index.html`:**
- Sitio oficial del Club Taekwondo Dragón Rojo (no solo una guía)
- 7 secciones: Inicio, Acerca del club, Historia en Colombia, Acerca del Maestro, Guía examen cinta negra, Precio al mes, Contacto y redes
- Navegación fluida (SPA)
- Menú hamburguesa en móvil
- Guía de examen completamente integrada (sin cambios respecto al original)

✅ **Nueva carpeta `assets/`:**
- Logo del club
- Fotos del Maestro
- Historia del club
- Banner promocional

✅ **Actualización del video:**
- Iframe de YouTube actualizado con parámetros completos
- Embed directo (no carga dinámica)

¡Listo para subir! 화이팅!
