## base de datos empresa jardineria!
>  base de datos para empresa de jardinera , la base de datos esta especificada para una empresa que proveea de servicios a  casas o fraccionamientos esta ocupa gran parte de las necesidades 
## income (ED)
***Income_ID (PK)*, Date, Type, Amount, Description, *Client_id(FK)*** . descripcion un ingreso es un pago recibido al negocio.

## person (ED)
***Client_ID(PK)*, Name, role, Surname, phone Number, Email**, una persona es el individuo que es un cliente o  un empleado

## role (ED)
***roles_ID(PK)*, name, description**, un rol es lo que es asignado a un individuo puede ser un cliente o un empleado

## Client(EP)
***person_id(FK), contract_id,  place_id,  *income(FK)***, un cliente es el individuo o empresa que requiere los servicios de la empresa 

## employee (EP)
***person_id(FK),  *Salary(FK)***,un empleado es un individuo que trabaja para la empresa, y es pagado por el servicio que presta a la empresa 

##  spend (ED)
 ***Spent_ID(PK)*, amount, Date, description *category(FK)*, ***, un spend  es el gasto que se hace por ejemplo al adquirir gasolina , una planta , herramientas, vehiculos o cualquier cosa de uso para la empresa

## category (ED) 
 ***category_ID(PK)*,name ***, categorias en las cuales la empresa gasta su dinero

## payment (ED)
***Payment_ID(PK)*, Amount, Date, Type, Hrs_Worked, Description**, el pago dado a un empleado
## contract (ED)
**Contract_ID(PK)*, Price, Date*, End_Date, Renewal_Period, Description, *Client(FK)***   un contrato es un documento escrito entre negocio y el cliente para acordar los servicios
## aditional_service(ED)
***Service_ID(PK)*, Price, Description, PLACE_ID**,un servicio adicional no se especifica en el contrato pero se lleva a cabo dentro del lugar




## place(ED)
***Place_ID(PK)*, Address, Start_Date, End_Date**, el lugar es la localizacion donde se llevara a cabo el servicio


## vehicle(ED)
***Car_ID(PK)* name,  car_type, un auto es un vehiculo usado por un empleado o varios empleados para transportar herramientas y llevar a cabo servicios.


# Relaciones
* Empleado recibe pago; un empleado puede recibir muchos pagos :  1 - N
 * Empleado asignado a vehiculo; un empleado o varios empleados pueden ser asignados a un vehiculo :  N - 1
 * vehiculo que  contiene herramientas; una o varias herramientas son asignadas a un vehiculo : N - 1
  * vehiculo asignado a lugar; un vehiculo es asignado a un lugar : 1 - 1
  * lugar pertenciente a cliente;   1  - 1  
  * servicio adicional dado a luga : ardinality: un servicio adicional o varios servicios son dados a un lugar: N - 1
  * ingreso obtenido por cliente: un ingreso o varios ingresos son obtenidos por un cliente N -1 

# Reglas

### income 
- Crear el registro de un ingreso.
- Leer el registro de un ingreso dependiendo de un cliente.
- leer todos los ingresos.
- actualizar los datos de un ingreso.
- eliminar un ingreso si es incorrecto.

### person 
- crear el registro de una persona
- actualizar una persona
- eliminar los datos de una persona
- leer los datos de varias personas

### role 
- leer un rol
- leer varios roles
- asignar un rol a una persona
- crear un rol
- actualizar un rol
- eliminar un rol

### client  
- leer una persona con el rol de cliente
- leer varias personas con el rol de cliente

### employee
- leer una persona con el rol o roles de empleado
- leer varias personas con el rol de empleado

### spend
- crear el  registro de un gasto
- actualizar un gasto
- eliminar un gasto
-  leer un gasto
- leer varios gasto

### category

- crear un registro de category
- actualizar una category
- leer una category
- leer varias categories

### payment

- crear el registro de un pago asignado a una persona con el rol de empleado
- leer un pago
- leer varios pagos
- actualizar un pago
- eliminaar un pago

### contract 

- crear un registro de contrato
- leer un contrato
- leer varios contratos
- actualizar un contrato

### aditional_service

- crear un registro de  un servicio adiconal
- leer un servicio adicional
- leer varios servicios adicionales
- actualizr un servicio adicional

### place

- crear un registro de un lugar
- leer un lugar
- leer varios lugares
- eliminar un lugar

###  vehicle

- crear  el registor de un vehiculo 
-  leer un vehiculo
- leer varios vehiculos
- eliminar un vehiculo
