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
***Car_ID(PK)*, Start_Date, End_Date, Car_Desc**, un auto es un vehiculo usado por un empleado o varios empleados para transportar herramientas y llevar a cabo servicios.
## herramienta
***Tool_ID(PK)*, Brand, Name, Description, Price**.una herramienta es un utensilio que sera usado por un empleado o  varios empleados que seran usados en el lugar donde se llevan a cabo los servicios.

# Relaciones
* Empleado recibe pago; Cardinality: 1..N; Participation: Total, Total
 * Empleado asignado a vehiculo Cardinality: N..1; Participation: Total, Total 
 * vehiculo que  contiene herramientas; Cardinality: 1..N; Participation: Total, Total
  * auto asignado a lugar; Cardinality: 1..1; Participation: Total, Total 
  * lugar pertenciente a cliente; Cardinality: N..1; Participation: Partial, Total 
  * servicio adicional dado a lugar; Cardinality: N..1; Participation: Partial, Total 
  * ingreso obtenido por cliente; Cardinality: N..1; Participation: Total, Total
