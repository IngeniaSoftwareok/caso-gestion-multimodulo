# Decisiones técnicas

## Validar la empresa en el backend

La separación de datos se aplica en el servidor. Cada consulta y operación toma la empresa de la sesión y valida los permisos del usuario, además de los filtros que se muestran en la interfaz.

## Identificar los reintentos

Si se pierde una respuesta, el cliente puede volver a enviar la solicitud. Incorporé una clave de idempotencia por empresa para reconocer ese reintento y evitar registrar la operación dos veces.

## Compartir servicios entre módulos

Catálogo, clientes, ventas, compras, caja y stock utilizan una base común. Esta organización me permite mantener reglas compartidas y ampliar el producto sin resolver cada módulo como una aplicación separada.

## Habilitar módulos por empresa

La configuración define qué módulos utiliza cada empresa y qué permisos tiene cada usuario. Las dependencias entre módulos se mantienen dentro del producto.
