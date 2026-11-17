 PixelPro — TP7

**Instalación previa:** colocar `PixelPro/` en `C:\xampp\htdocs\`, encender Apache y MySQL, importar `PixelPro/database/schema.sql` en phpMyAdmin y configurar `PixelPro/config/.env` a partir de `.env.example` sin compartir las credenciales. Abrir `http://localhost/PixelPro/`.

## Objetivo

Implementar operaciones CRUD sobre MySQL utilizando PDO y consultas preparadas.

## Implementación

El CRUD administra la tabla **`juegos`**, con categoría asociada mediante `categorias_juego`:

- **Create:** `admin/crear.php` agrega juegos.
- **Read:** `admin/index.php` lista y permite buscar juegos mediante GET.
- **Update:** `admin/editar.php?id=...` cambia un juego existente.
- **Delete:** `admin/eliminar.php` recibe POST y verifica el token CSRF antes de eliminar.
- `admin/categorias.php`: alta y consulta de categorías.
- `config/conexion.php`: conexión PDO.

## Cómo demostrarlo

1. Iniciá sesión con una cuenta con rol `admin`. Abrí `http://localhost/PixelPro/admin/index.php`.
2. Sacá la captura del listado. Después entrá en **Crear juego**, escribí un nombre de prueba, seleccioná una categoría y guardalo.
3. En la tabla, presioná **Editar** sobre ese juego, cambiá la descripción y guardá.
4. Volvé al listado, hacé clic en **Eliminar** y aceptá la confirmación solo para el registro de prueba.
5. Si no podés entrar al administrador, primero completá TP8 y asigná tu usuario de prueba al rol `admin` en tu instalación local.


## Evidencias fotográficas (capturas reales)

Las siguientes imágenes están guardadas en la carpeta **`capturas de limon/capturas ayala tp7/`**. Los enlaces son relativos a este README ubicado en `PixelPro/docs/`. Se respetaron los nombres originales, incluidos los dos espacios del TP5.



## Evidencias fotográficas (capturas reales)

### Listado de juegos

![Listado de juegos](tp7-listado.png)

### Crear un juego

![Crear un juego](tp7-crear.png)

### Editar un juego

![Editar un juego](tp7-editar.png)

### Eliminar un juego

![Eliminar un juego](tp7-eliminar.png)
