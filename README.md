# consultas2_sql

## Modelo Físico

![Modelo fisico](img/Empresa.jpg "Modelo fisico")

## Tabla Empleados

![Modelo fisico](img/captura1.png "Modelo fisico")


1. Obtener la lista de los apellidos de todos los empleados.

`SELECT apellidos_empleado FROM Empleado;`

![Modelo fisico](img/captura2.png "Modelo fisico")

2. Obtener los apellidos de todos los empleados sin repeticiones.

`SELECT DISTINCT apellidos_empleado FROM Empleado;`

![captura3](img/captura3.png "captura3")

3. Obtener todos los datos de los empleados que se apellidan 'Gomez'.

`SELECT * FROM Empleado WHERE apellidos_empleado = 'Gomez';`

![captura4](img/captura4.png "captura4")

4. Obtener todos los datos de los empleados que se apellidan "Diaz" y los que se apellidan "Rodriguez".  Usar OR o IN

`SELECT * FROM Empleado WHERE apellidos_empleado IN ('Rodriguez', 'Diaz');`

![captura5](img/captura5.png "captura5")

5. Obtener los nombres de los empleados que trabajan en el departamento 11

`SELECT nombre_empleado FROM Empleado WHERE id_departamento = 11;`

![captura6](img/captura6.png "captura6")

6. Obtener todos los datos de los empleados cuyo apellido empiece por 'P'

`SELECT * FROM Empleado WHERE apellidos_empleado LIKE 'P%';`

![captura7](img/captura7.png "captura7")

7. Obtener el presupuesto total de todos los departamentos.

`SELECT SUM(presupuesto_departamento) AS presupuesto_departamento FROM Departamento;`

![captura8](img/captura8.png "captura8")

8. Obtener el número de empleados de cada departamento.

`SELECT id_departamento, COUNT(*) AS numero_empleados FROM Empleado GROUP BY id_departamento;`

![captura9](img/captura9.png "captura9")

9. Obtener un listado completo de empleados, incluyendo por cada empleado los datos del empleado y de su departamento.

`SELECT * FROM Empleado JOIN Departamento ON Empleado.id_departamento = Departamento.id_departamento;`

![captura10](img/captura10.png "captura10")

10. Obtener un listado completo de empleados, incluyendo el nombre y apellidos del empleado junto al nombre y presupuesto de su departamento.

`SELECT e.nombre_empleado, e.apellidos_empleado, d.nombre_departamento, d.presupuesto_departamento FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento;`

![captura11](img/captura11.png "captura11")

11. Obtener los nombres y apellidos de los empleados que trabajen en departamentos cuyo presupuesto sea mayor a 100000000

`SELECT e.nombre_empleado,e.apellidos_empleado FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento WHERE d.presupuesto_departamento > 100000000;`

![captura12](img/captura12.png "captura12")

# Cláusula inner join

![innerjoin](img/innerjoin.png "innerjoin")

# Cláusula subconsulta

![subconsulta](img/subconsulta.png "subconsulta")