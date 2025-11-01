Documentación API
=================

Autenticación:

- Registro: ``POST /auth/register``
- Login: ``POST /auth/login``

Usuarios:

- ``GET /user/me`` Obtener perfil
- ``PUT /users/me`` Actualizar perfil
- ``DELETE /users/me`` Eliminar cuenta
- ``GET /users/reactivar/{users_id}`` Reactivar cuenta (Solo para bibliotecarios)

Lista de deseos:

- ``GET /wishlist/list`` Ver lista
- ``POST /wishlist/add`` Agregar libro
- ``DELETE /wishlist/delete/{book_id}`` Quitar libro
- ``POST /wishlist/ensure-book-for-loan`` Asegurar libro para préstamo
- ``GET /wishlist/buscar-libro/{openlibrary_key}`` Busca el libro por su clave OpenLibrary

Reviews:

- ``POST /reviews/rate`` Sube una calificación
- ``GET /reviews/ratings/{openlibrary_key}`` Obtiene calificaciones de un libro
- ``GET /reviews/commets/{openlibrary_key}`` Obtiene comentarios de un libro
- ``POST /reviews/comment`` Sube un comentario
- ``GET /reviews/user-rating/{openlibrary_key}`` Obtiene la calificación del usuario para un libro
- ``PUT /reviews/comments/{comment_id}`` Actualiza un comentario
- ``DELETE /reviews/comments/{comment_id}`` Elimina un comentario

Recuperación de contraseña:

- ``POST /auth/recuperar-contrasena`` Solicitar restablecimiento
- ``POST /auth/restablecer-contrasena`` Restablecer contraseña

Préstamos (Digital):

- ``POST /prestamos/digital`` Registra préstamo digital

Préstamos (Físico):

- ``POST /prestamos-fisicos/solicitar`` Solicitar préstamo físico
- ``GET /prestamos-fisicos/mis-prestamos`` Ver préstamos físicos del usuario
- ``PUT /prestamos-fisicos/cancelar/{prestamo_id}`` Cancelar préstamo físico
- ``PUT /prestamos-fisicos/estado/{prestamo_id}`` Cambiar estado del préstamo (Solo bibliotecarios)