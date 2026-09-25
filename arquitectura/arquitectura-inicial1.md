```mermaid
    flowchart TB


    subgraph ACTORES["Actores"]
        direction LR
        Cliente["Cliente"]
        Seller["Seller"]
        Administrador["Administrador"]
    end

    subgraph PRESENTACION["Presentacion"]
        direction LR
        AppWeb["Aplicacion Web"]
        API["API REST"]
    end

    subgraph NEGOCIO["Negocio"]
        direction LR
        M_Usuarios["Usuarios"]
        M_Sellers["Sellers"]
        M_Catalogo["Catalogo"]
        M_Carrito["Carrito"]
        M_Pedidos["Pedidos"]
    end

    subgraph DATOS["Datos"]
        BD[("Base de Datos")]
    end

    subgraph EXTERNOS["Sistemas Externos"]
        direction LR
        PasarelaPago["Pasarela de Pago"]
        ServicioEnvio["Servicio de Envio"]
    end

    Cliente --> AppWeb
    Seller --> AppWeb
    Administrador --> AppWeb

    AppWeb --> API

    API --> M_Usuarios
    API --> M_Sellers
    API --> M_Catalogo
    API --> M_Carrito
    API --> M_Pedidos

    M_Usuarios --> BD
    M_Sellers --> BD
    M_Catalogo --> BD
    M_Carrito --> BD
    M_Pedidos --> BD

    M_Pedidos --> PasarelaPago
    M_Pedidos --> ServicioEnvio```