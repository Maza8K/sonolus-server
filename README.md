
# 🎵 Servidor Sonolus: Esclava

## 📊 Info del Nivel
- **BPM detectado**: 95
- **Motor**: Project Sekai (PJSEKAI)
- **Carriles**: 5

## 🚀 Cómo subir a GitHub Pages

### 1. Crear repositorio en GitHub
- Ve a github.com y crea un repositorio nuevo (público)
- Nombre sugerido: `mi-sonolus-server`

### 2. Subir archivos
Sube TODO el contenido de esta carpeta (`sonolus-server/`) al repositorio.

### 3. Activar GitHub Pages
- Ve a Settings → Pages
- Source: Deploy from a branch
- Branch: main / root
- Guarda

### 4. Obtener URL
Tu servidor estará en: `https://TUUSUARIO.github.io/mi-sonolus-server/`

### 5. Agregar en Sonolus
1. Abre Sonolus en tu celular
2. Ve a Settings → Servers → Add
3. Pon la URL de GitHub Pages
4. ¡Juega!

## ⚠️ IMPORTANTE: Motor de Project Sekai

Los archivos del motor (EnginePlayData, EngineWatchData, etc.) son **placeholders**.
Para que funcione correctamente, necesitas obtener los archivos reales:

### Opción A: Desde npm (requiere Node.js)
```bash
npm install sonolus-pjsekai-engine
# Copia los archivos de node_modules/sonolus-pjsekai-engine/ 
# a la carpeta engines/pjsekai/
```

### Opción B: Desde servidor existente
Descarga los archivos del motor desde un servidor de Sonolus existente
y colócalos en `engines/pjsekai/`.

### Opción C: Usar servidor que ya tiene el motor
En lugar de tu propio servidor, sube solo el nivel a un servidor
comunitario que ya tenga PJSEKAI instalado.

## 📝 Estructura del Servidor
```
sonolus-server/
├── info.json              ← Info del servidor
├── levels/
│   ├── index.json         ← Índice de niveles
│   └── esclava/
│       ├── item.json      ← Metadatos
│       ├── data.json      ← Chart (debug)
│       ├── data.json.gz   ← Chart (comprimido)
│       ├── bgm.mp3        ← Canción
│       ├── preview.mp3    ← Preview
│       └── cover.png      ← Portada
└── engines/
    ├── index.json         ← Índice de motores
    └── pjsekai/
        ├── item.json      ← Info del motor
        └── ...            ← Archivos del motor
```

## 🔧 Personalización

Para regenerar el nivel con diferentes parámetros:
```bash
python sonolus-auto-generator.py tu-cancion.mp3     --title "Nuevo Titulo"     --artist "Nuevo Artista"     --difficulty "Expert"     --level 25     --density 1.5
```

## 📚 Recursos
- Sonolus Wiki: https://wiki.sonolus.com
- Sonolus.js: https://wiki.sonolus.com/sonolus.js-guide
- PJSEKAI Engine: https://github.com/NonSpicyBurrito/sonolus-pjsekai-engine
