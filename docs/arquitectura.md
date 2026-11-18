# Arquitectura del caso

Vista conceptual de la plataforma; los nombres representan responsabilidades, no infraestructura productiva publicada.

```mermaid
flowchart LR
  D["Cliente de escritorio · JavaFX"] --> A["API central · Spring Boot"]
  A --> C["Contexto de empresa y permisos"]
  C --> V["Módulos de negocio"]
  V --> M["Persistencia · MySQL"]
  V --> X["Catálogo / Clientes / Ventas / Compras / Caja / Stock"]
```

El cliente consume la API: no es una aplicación web ni una herramienta completamente sin conexión. Los módulos forman parte del build y se habilitan según la empresa.

El núcleo conserva responsabilidades transversales y los módulos organizan el negocio. Esta presentación no distribuye tablas internas, scripts de despliegue, secretos o una copia del producto.
