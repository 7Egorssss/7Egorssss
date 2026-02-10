# ⚽ AgusChampion 2026

Aplicación web moderna para gestionar tu liga escolar con clasificación en tiempo real y seguimiento de todas las jornadas.

## 🚀 Características

- ✅ **Tabla de Clasificación**: Muestra la posición de cada equipo con puntos, partidos jugados, goles a favor/contra y diferencia de goles
- ✅ **Visualización de Jornadas**: Ve todos los partidos organizados por jornada con resultados destacados
- ✅ **Actualización desde GitHub**: Solo el administrador puede actualizar resultados editando el JSON
- ✅ **Cálculo Automático**: Las estadísticas se calculan automáticamente desde el JSON
- ✅ **Ganadores Destacados**: Los equipos ganadores aparecen en verde brillante
- ✅ **Diseño Champions League**: Fondo oscuro con patrón de balones de fútbol
- ✅ **100% Responsive**: Funciona en móviles, tablets y PC

## 📦 Cómo usar con GitHub Pages

### Opción 1: Crear desde cero

1. **Crea un nuevo repositorio en GitHub**
   - Ve a https://github.com/new
   - Ponle un nombre como `liga-escolar`
   - Marca como "Public"
   - Click en "Create repository"

2. **Sube los archivos**
   - Click en "uploading an existing file"
   - Arrastra los archivos `index.html` y `liga-data.json`
   - Click en "Commit changes"

3. **Activa GitHub Pages**
   - Ve a Settings → Pages
   - En "Source" selecciona "main" branch
   - Click en "Save"
   - ¡Tu página estará disponible en unos minutos en `https://tu-usuario.github.io/liga-escolar`!

### Opción 2: Usar Git (si tienes Git instalado)

```bash
# Crear repositorio local
git init
git add index.html liga-data.json README.md
git commit -m "Initial commit - Liga Escolar"

# Conectar con GitHub (crea primero el repositorio en GitHub)
git remote add origin https://github.com/TU-USUARIO/liga-escolar.git
git branch -M main
git push -u origin main
```

Luego activa GitHub Pages en Settings → Pages.

## 📝 Cómo usar la aplicación

### Ver la Clasificación
- Click en "CLASIFICACIÓN" para ver la tabla de posiciones
- Los 3 primeros equipos aparecen destacados con fondo dorado
- La tabla se calcula automáticamente desde los resultados del JSON

### Ver las Jornadas
- Click en "JORNADAS" para ver todos los partidos
- Muestra qué equipo descansa en cada jornada
- **Los partidos jugados muestran el resultado** con el marcador
- **El equipo ganador aparece destacado en verde brillante** ✅
- **Los empates aparecen en amarillo** 🟡
- **Los partidos sin jugar muestran "VS"**

### 📊 Actualizar Resultados - Solo desde GitHub

La aplicación está configurada para que **solo tú puedas actualizar los resultados** editando el archivo JSON en GitHub. Esto evita que cualquier visitante pueda modificar la liga.

**Pasos para actualizar resultados:**

1. **Ve a tu repositorio en GitHub**
2. **Click en `liga-data.json`**
3. **Click en el icono del lápiz (Edit)**
4. **Agrega los resultados** en el formato:

```json
{
  "local": "Equipo 1",
  "visitante": "Equipo 9",
  "golesLocal": 3,
  "golesVisitante": 1
}
```

5. **Click en "Commit changes"**
6. **Espera 1-2 minutos** para que GitHub Pages actualice
7. **Recarga la página web** (Ctrl+F5 o Cmd+Shift+R)
8. ¡Los resultados y clasificación se actualizan automáticamente!

**Ejemplo completo de una jornada con resultados:**
```json
{
  "nombre": "Jornada 1",
  "descansa": "Equipo 5",
  "partidos": [
    { 
      "local": "Equipo 1", 
      "visitante": "Equipo 9", 
      "golesLocal": 3, 
      "golesVisitante": 1 
    },
    { 
      "local": "Equipo 2", 
      "visitante": "Equipo 8", 
      "golesLocal": 2, 
      "golesVisitante": 2 
    },
    { 
      "local": "Equipo 3", 
      "visitante": "Equipo 7"
      // Sin resultados aún - se mostrará como "VS"
    }
  ]
}
```


### Resetear la Liga

Si quieres empezar de cero, simplemente edita el `liga-data.json` en GitHub y elimina los campos `golesLocal` y `golesVisitante` de todos los partidos, o ponlos en 0.

**Ejemplo de partido reseteado:**
```json
{
  "local": "Equipo 1",
  "visitante": "Equipo 9"
  // Sin golesLocal ni golesVisitante
}
```

## 🎨 Personalización

### Cambiar los nombres de los equipos

Edita el archivo `liga-data.json` y cambia los nombres:

```json
"equipos": {
  "Los Tigres": { ... },
  "Las Águilas": { ... },
  ...
}
```

También actualiza los nombres en cada partido de las jornadas.

### Cambiar los colores

En el archivo `index.html`, busca la sección `:root` en el CSS y modifica:

```css
:root {
    --primary: #FF3B30;    /* Color principal (rojo) */
    --secondary: #FFD60A;  /* Color secundario (amarillo) */
    --accent: #00D4FF;     /* Color de acento (azul) */
    --dark: #1C1C1E;       /* Fondo oscuro */
}
```

## 💾 Almacenamiento de Datos

Los resultados están **directamente en el archivo `liga-data.json`** en GitHub. Esto significa:
- ✅ Los datos son permanentes y controlados por ti
- ✅ Solo tú (el dueño del repositorio) puedes actualizar los resultados
- ✅ Los visitantes solo pueden ver la liga, no pueden modificarla
- ✅ El historial de cambios queda guardado en GitHub
- ✅ No se necesita base de datos ni servidor

**Ventajas de este sistema:**
- 🔒 **Seguro**: Nadie puede modificar tus resultados sin acceso a tu GitHub
- 📝 **Transparente**: Todos los cambios quedan registrados en GitHub
- 🆓 **Gratis**: No necesitas pagar por hosting o base de datos
- 📱 **Accesible**: Puedes actualizar desde cualquier dispositivo con acceso a GitHub

## 🔧 Tecnologías Utilizadas

- HTML5
- CSS3 (animaciones, gradientes, efectos)
- JavaScript vanilla (sin frameworks)
- Google Fonts (Bebas Neue, Archivo)
- LocalStorage API

## 📱 Responsive

La aplicación es completamente responsive y funciona en:
- 💻 Computadoras
- 📱 Tablets
- 📱 Móviles

## 🆘 Soporte

Si tienes problemas:
1. Asegúrate de que GitHub Pages esté activado
2. Verifica que ambos archivos (`index.html` y `liga-data.json`) estén en la raíz del repositorio
3. Espera unos minutos después de activar Pages

## 📄 Licencia

Libre para usar en tu escuela o proyecto personal. ¡Diviértete! ⚽

---

Hecho con ❤️ para AgusChampion 2026
