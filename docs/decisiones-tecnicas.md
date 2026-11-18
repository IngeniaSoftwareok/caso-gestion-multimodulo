# Decisiones seleccionadas

## Mantener el contexto de empresa

Los datos y permisos de una operación deben corresponder a la empresa de la sesión. La separación multiempresa es una responsabilidad del backend, no sólo de los filtros visuales del cliente.

## Evitar duplicaciones por reintentos

Una respuesta perdida no debe implicar registrar dos veces la misma solicitud. La implementación revisada incluye reservas y comprobaciones de idempotencia por empresa y clave. El recorrido visual incluido no reemplaza una prueba específica de este comportamiento.

## Conectar módulos sin anunciar una oferta ilimitada

Los módulos tienen dependencias y habilitación por empresa. Mostrar varias pantallas no implica que todo módulo esté habilitado en cualquier instalación o plan.

## Distinguir la beta de la aceptación externa

Existen ensayos locales y LAN. La entrega productiva, las condiciones comerciales y la adopción por empresas son cuestiones distintas. El producto se presenta como beta cerrada y gestión interna; no como facturación fiscal electrónica.
