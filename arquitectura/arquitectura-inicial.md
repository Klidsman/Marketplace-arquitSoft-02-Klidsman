```mermaid
    flowchart TB
    subgraph CAPA1["Capa de Presentacion"]
        direction LR
        UI_Cliente["Interfaz Cliente Web App"]
        UI_Seller["Interfaz Seller Web App"]
        UI_Admin["Interfaz Administrador Web App"]
    end

    API["API REST Gateway de comunicacion"]

    subgraph CAPA2["Capa de Logica de Negocio"]
        direction LR
        M_Catalogo["Modulo Catalogo"]
        M_Productos["Modulo Productos"]
        M_Carrito["Modulo Carrito"]
        M_Pedidos["Modulo Pedidos"]
        M_Pagos["Modulo Pagos"]
        M_Sellers["Modulo Sellers"]
        M_Usuarios["Modulo Usuarios"]
        M_Ventas["Modulo Ventas"]
    end

    subgraph CAPA3["Capa de Datos"]
        direction LR
        BD[("Base de Datos Transaccional")]
    end

    subgraph EXT["Servicios Externos"]
        direction LR
        PasarelaPago["Pasarela de Pago"]
        ServicioEnvio["Servicio de Envio"]
        ServicioFacturacion["Servicio de Facturacion"]
        ERP["ERP Productos y Stock"]
    end

    UI_Cliente --> API
    UI_Seller --> API
    UI_Admin --> API

    API --> M_Catalogo
    API --> M_Productos
    API --> M_Carrito
    API --> M_Pedidos
    API --> M_Pagos
    API --> M_Sellers
    API --> M_Usuarios
    API --> M_Ventas

    M_Catalogo --> BD
    M_Productos --> BD
    M_Carrito --> BD
    M_Pedidos --> BD
    M_Pagos --> BD
    M_Sellers --> BD
    M_Usuarios --> BD
    M_Ventas --> BD

    M_Catalogo --> ERP
    M_Productos --> ERP
    M_Pagos --> PasarelaPago
    M_Pedidos --> ServicioEnvio
    M_Pedidos --> ServicioFacturacion```

