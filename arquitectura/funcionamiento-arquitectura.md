
    | Capa | Pregunta que responde | Respuesta |
|------|---------------------------|--------------|
| Presentación | ¿Cómo interactúa el usuario? | A través de interfaces web (Cliente, Seller, Administrador) que consumen la API REST para buscar productos, gestionar el carrito, realizar pedidos, pagar, y administrar la plataforma según el rol. |
| Lógica de negocio | ¿Qué hace el sistema? | Procesa las reglas y operaciones del marketplace mediante módulos independientes (catálogo, productos, carrito, pedidos, pagos, sellers, usuarios, ventas), coordinando la comunicación con la base de datos y los servicios externos (pasarela de pago, envío, facturación, ERP). |
| Datos | ¿Dónde se almacena la información? | En una base de datos transaccional que guarda productos, carritos, pedidos, usuarios, ventas y demás información persistente del sistema. |