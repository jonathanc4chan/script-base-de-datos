# script-base-de-datos

-- Crear la tabla Material
CREATE TABLE Material (
    id INT PRIMARY KEY,
    cantidad DECIMAL,
    medida VARCHAR(255),
    nombre VARCHAR(255)
);

-- Crear la tabla Factura
CREATE TABLE Factura (
    nit INT PRIMARY KEY,
    nombre VARCHAR(255)
);

-- Crear la tabla Producto
CREATE TABLE Producto (
    codigo INT PRIMARY KEY,
    descripcion VARCHAR(255),
    precio DECIMAL
);

-- Crear la tabla Cliente
CREATE TABLE Cliente (
    id INT PRIMARY KEY,
    nombre VARCHAR(255),
    pago DECIMAL
);

-- Crear la tabla Orden
CREATE TABLE Orden (
    numero INT PRIMARY KEY,
    fecha DATE,
    vendedor VARCHAR(255),
    cliente_id INT,
    FOREIGN KEY (cliente_id) REFERENCES Cliente(id)
);
