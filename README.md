# CONSULTAS_SQL_1
# INtroduccion a las consultas a una BD usando el lenguaje SQL 

## Base de datos: Ventas 
## Tabla: Cliente 

![Tabla_Cliente](./img/Tabla.Cliente.png)

## Instruccion SELECT
- permite seleccionar datos de una tabla.
-su formato es: 'SELECT campos_tablas FROM nombre_tabla''

### Consulta No. 1
1. Para visualizar toda la informacion que contiene la tabla Cliente se puede incluir con la instruccion SELECT el caracter **\*** o cada uno de los campos de la tabla.

- 'SELECT * FROM cliente'
![consulta1](./img/consulta_1_.png "consulta 1 - 1")

- 'SELECT identificacion, nombre, apellidos, direccion, telefono, ciudad_nac, fecha_nac FROM Cliente'
![consulta2](./img/consulta1_2.png "Consulta 1 - 2")

### Consulta No. 2

2. Para visualizar solamente la identificacion del Cliente: 'SELECT identificacion FROM Cliente'
![consulta2](./img/3.png)

### Consulta No.3

3. si se desea obtener los registros cuya identificacion sea mayor o igual a 150, se debe utilizar la clausula 'WHERE' que especifica las condiciones que deben reunir los registros que se van a seleccionar: 'SELECT * FROM Cliente WHERE identificacion>=150

![consultas3](./img/consulta3.png)

### Consulta No. 4 

4. Sedesea obtener los registros cuyos apellidos sean vanegas o cetina, se debe utilizar el operador IN que especifica los registros que se quieren visualizar de una tabla.

'SELECT apellidos FROM Cliente WHERE apellidos IN('Vanegas', 'Cetina')

![consulta4_1](./img/4%20(1).png)

O se puede utilizar el operador 'OR'

'SELECT apellidos,nombre FROM Clientes WHERE apellidos = 'Vanegas' OR apellidos = 'Cetina'

![consulta4_2](./img/consulta4_2.png)

### Consulta No. 5

5. Se a menor que 110 y la ciudad sea cali, se debe utilizar el operador 'AND' 

'SELECT * FROM Clientes WHERE identificacion<=110 AND ciudad_nac = 'Cali'

![Consulta5](./img/Consulta5.png)

### Consulta No. 6 

6. Si se desea obtener los registros cuyos nombres empiecen por la letra 'A', se debe utilizar el operador 'LIKE' que utiliza los patrones '%' (todos) y '_' (Caracter).

'SELECT * FROM Clientes WHERE nombre LIKE 'A%'

![consultas6](./img/6%20(1).png)

### Consulta No. 7

7. Se desea obtener los registros cuyos nombres contengan la letra 'a'

'SELECT * FROM cliente WHERE nombre LIKE '%a%'

![consultas7](./img/7%20(1).png)

### Consulta No. 8

8. Se desea obtener los registros donde la cuarta letra del nombre del cliente sea la letra 'a' 

'SELECT * FROM Cliente WHERE nombre LIKE '___a'

![consultas8](./img/8%20(1).png)

### Consultas No. 9 

9. Si se desea obtener los registros cuya identificacion este entre el intervalo 110 y 150, se debe utilizar la clausula 'BETWEEN' que sirve para especificar un intervalo de vaores.

'SELECT * FROM Clientes WHERE identificacion BETWEEN 110 AND 150

![consultas9](./img/9%20(1).png)

## Instruccion DELETE
-Permite borrar todos o un grupo especifico de registros de una tabla.
- Su formato es: 'DELETE FROM nombre_tabla'

### Eliminacion No. 1

1. Eliminar los registros cuya identificacion sea mayor a 170

'DELETE FROM cliente WHERE identificacion > 170'

![Eleminacion](./img/Delete.png)

2. Eliminar los reistros cuya identificacion sea igual a 116

'DELETE FROM Clientes WHERE identificacion = 116'

## Instruccion UPDATE
-Permite actualizar un campo de una tabla.
- Su formato es: 'UPDATE nombre_tabla SET nombre campo = valor'

### Actualizacion No. 1

1. Para actualizar la ciudad de nacimiento de cristian vanegas, cuya identificacion es 114

'UPDATE Cliente set Ciudad_nac = 'Pereira' WHERE identificacion=114'

![actualizacion](./img/actualisacon.png)

## Creacion tabla Cliente

### Diccionario de datos
|Campo|Tipo de dato|Longitud|
|-----|------------|--------|
|***no_pedido**| varchar|15|
|iden_cliente|varchar|15|
|fecha_compra|date||
|fecha_vencimiento|date||
|observacion|varchar|30|

### Modelo Entidad - Relacion
![modelo](./img/Modelo.png)

### Tabla de pedidos

![pedidios](./img/Pedidos.png)