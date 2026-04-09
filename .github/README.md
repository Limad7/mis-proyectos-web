# Workflows para GitHub Pages

Este directorio contiene los workflows para desplegar tus proyectos web en GitHub Pages.

## 📁 Archivos:

### deploy.yml
- Despliega el proyecto activo actual
- Configurado para desplegar `noelia-yoga/`

### workflows-template.yml
- Plantilla para crear nuevos workflows
- Reemplaza `[PROJECT-NAME]` y `[PROJECT-FOLDER]`

## 🚀 Crear un nuevo workflow:

1. **Copia la plantilla:**
   ```bash
   cp workflows-template.yml deploy-[nombre].yml
   ```

2. **Edita el archivo:**
   - Reemplaza `[PROJECT-NAME]` con el nombre de tu proyecto
   - Reemplaza `[PROJECT-FOLDER]` con el nombre de la carpeta

3. **Ejemplo:**
   ```yaml
   name: Deploy MiNuevoProyecto to GitHub Pages
   on:
     push:
       branches: [ main ]
       paths:
         - 'mi-nuevo-proyecto/**'  # Carpeta del nuevo proyecto
   ```

4. **Commitea el cambio:**
   ```bash
   git add deploy-mi-nuevo-proyecto.yml
   git commit -m "Añadir workflow para MiNuevoProyecto"
   ```

## 📝 Notas:
- Cada proyecto necesita su propio workflow
- Los nombres de workflow deben ser únicos
- Los proyectos se desplegarán automáticamente al hacer push