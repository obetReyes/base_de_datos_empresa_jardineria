## base de datos empresa jardineria!
## ingreso
***Income_ID (PK)*, Date, Type, Amount, Description** . descripcion un ingreso es un pago recibido al negocio.
## client
***Client_ID(PK)*, Name, Address, Phone Number, Email**, un cliente es el individuo o empresa que requiere los servicios de la empresa 
## empleado
***Employee_ID(PK)*, Name, Address, Phone Number, *Salary(FK)****,un empleado es un individuo que trabaja para la empresa, y es pagado por el servicio que presta a la empresa
## pago
***Payment_ID(PK)*, Amount, Date, Type, Hrs_Worked, Description**, el pago dado a un empleado
## contrato
***Contract_ID(PK)*, Price, Description**, un contrato es un documento escrito entre negocio y el cliente para acordar los servicios
## servicio adicional
***Service_ID(PK)*, Price, Description**,un servicio adicional no se especifica en el contrato pero se lleva a cabo dentro del lugar
## lugar
***Place_ID(PK)*, Address, Start_Date, End_Date**, el lugar es la localizacion donde se llevara a cabo el servicio

## vehiculo
***Car_ID(PK)*, Start_Date, End_Date, Car_, un auto es un vehiculo usado por un empleado o varios empleados para transportar herramientas y llevar a cabo servicios.
## herramienta
***Tool_ID(PK)*, Brand, Name, Description, Price**.una herramienta es un utensilio que sera usado por un empleado o  varios empleados que seran usados en el lugar donde se llevan a cabo los servicios.

# Relaciones
* Empleado recibe pago; un empleado puede recibir muchos pagos :  1 - N
 * Empleado asignado a vehiculo; un empleado o varios empleados pueden ser asignados a un vehiculo :  N - 1
 * vehiculo que  contiene herramientas; una o varias herramientas son asignadas a un vehiculo : N - 1
  * vehiculo asignado a lugar; un vehiculo es asignado a un lugar : 1 - 1
  * lugar pertenciente a cliente;   1  - 1  
  * servicio adicional dado a luga : ardinality: un servicio adicional o varios servicios son dados a un lugar: N - 1
  * ingreso obtenido por cliente: un ingreso o varios ingresos son obtenidos por un cliente N -1 

