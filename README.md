---

# AgusChampion 2026

Gestor de ligas escolares diseñado para la visualización de resultados y clasificación en tiempo real mediante el procesamiento de datos estáticos.

---

### Funciones Principales

* **Tabla de Posiciones**: Cálculo automático de puntos y desempate por goles a favor.
* **Gestión de Jornadas**: Visualización de encuentros, marcadores y equipos en descanso.
* **Arquitectura Estática**: No requiere bases de datos complejas; funciona íntegramente con archivos HTML y JSON.
* **Diseño Adaptable**: Interfaz optimizada para su visualización en dispositivos móviles y ordenadores.

---

### Instalación Rápida

1. Subir los archivos `index.html` y `liga-data.json` a un repositorio de GitHub.
2. Acceder a la configuración del repositorio (**Settings > Pages**).
3. Seleccionar la rama **main** y guardar para generar el enlace público.

---

### Gestión de Resultados

Para actualizar la liga, los cambios se realizan directamente en el archivo `liga-data.json` desde GitHub.

**Formato de entrada de datos:**

```json
{
  "local": "Equipo A",
  "visitante": "Equipo B",
  "golesLocal": 2,
  "golesVisitante": 1
}

```

Si un partido no tiene resultados definidos, el sistema mostrará automáticamente el marcador como un enfrentamiento pendiente.

---

### Personalización de Estilos

El aspecto visual se controla mediante variables CSS en la cabecera del archivo `index.html`:

* **primary**: Tono principal para bordes y botones.
* **secondary**: Color de destaque para posiciones y marcadores.
* **accent**: Color de contraste para textos secundarios.

---

### Soporte Técnico

* **Seguridad**: Solo el propietario del repositorio puede modificar los resultados.
* **Persistencia**: Los datos se mantienen de forma permanente en el historial del repositorio.
