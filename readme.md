##1
```xml
/universidad/nombre/text()
```
```xml
Universidad de Victoria
```
##2
```xml
/universidad/pais/text()
```
```xml
España
```
##3
```xml
/universidad/carreras/carrera/nombre/text()
```
```xml
I.T. Informática
Dipl. Empresariales
Dipl. Relaciones Laborales
Lic. Quimica
Lic. Biología
Lic. Humanidades
```
##4
```xml
/universidad/carreras/carrera/plan/text()
```
```xml
2003
2001
2001
2003
2001
1980
```
##5
```xml
/universidad/alumnos/alumno/nombre/text()
```
```xml
Víctor Manuel
Luisa
Fernando
María
```
##6
```xml
/universidad/asignaturas/asignatura/@id
```
```xml
id="a01"
id="a02"
id="a03"
id="a04"
id="a05"
id="a06"
id="a07"
id="a08"
id="a09"
```
##7
```xml
/universidad/carreras/carrera[@id = "c01"]/*/text()
```
```xml
I.T. Informática
2003
250
Escuela de Informática
```
##8
```xml
/universidad/carreras/carrera[@id = "c02"]/centro/text()
```
```xml
Facultad de Ciencias Sociales
```
##9
```xml
/universidad/carreras/carrera[subdirector]/nombre/text()
```
```xml
Dipl. Relaciones Laborales
```
##10
```xml
/universidad/alumnos/alumno[estudios[proyecto]]/nombre/text()
```
```xml
Luisa
María
```
##11
```xml
/universidad/alumnos/alumno/estudios/carrera/@codigo
```
```xml
codigo="c01"
codigo="c02"
codigo="c02"
codigo="c01"
```
##12
```xml
/universidad/alumnos/alumno[@beca]/*[self::apellido1 or self::apellido2 or self::nombre]/text()
```
```xml
Pérez
Romero
Fernando
```
##13
```xml
/universidad/asignaturas/asignatura[@titulacion = "c04"]/nombre/text()
```
```xml
Pedagogía
Tecnología de los Alimentos
```

##14
```xml
/universidad/asignaturas/asignatura[trimestre = "2"]/nombre/text()
```
```xml
Ingeniería del Software
Pedagogía
Didáctica
Tecnología de los Alimentos
Historia del Pensamiento
```

##15
```xml
/universidad/asignaturas/asignatura[creditos_teoricos != "4"]/nombre/text()
```
```xml
Ofimática
Ingeniería del Software
Tecnología de los Alimentos
Bases de Datos
Historia del Pensamiento
```
##16
```xml
/universidad/alumnos/alumno[last()]/estudios/carrera/@codigo
```
```xml
codigo="c01"
```
##17
```xml
/universidad/alumnos/alumno[sexo = "Mujer"]/estudios/carrera/@codigo
```
```xml
codigo="c02"
codigo="c01"
```
##18
```xml
/universidad/alumnos/alumno[estudios[asignaturas[asignatura[@codigo="a02"]]]]/nombre/text()
```
```xml
Luisa
Fernando
María
```
##19
```xml
/universidad/alumnos/alumno[estudios[asignaturas[asignatura]]]/estudios/carrera/@codigo
```
```xml
codigo="c01"
codigo="c02"
codigo="c02"
codigo="c01"
```
##20
```xml
/universidad/alumnos/alumno[sexo="Hombre"]/*[self::apellido1 or self::apellido2]/text()
```
```xml
Rivas
Santos
Pérez
Romero
```
##21
```xml
//carrera[@id=//alumno[nombre="Víctor Manuel"]/estudios/carrera/@codigo]/nombre/text()
```
```xml
I.T. Informática
```
##22
```xml
//asignatura[@id=//alumno[nombre="Luisa"]/estudios/asignaturas/asignatura/@codigo]/nombre/text()
```
```xml
Ofimática
Ingeniería del Software
```
##23
```xml
//alumno[estudios/asignaturas/asignatura/@codigo=//asignatura[nombre="Ingeniería del Software"]/@id]/apellido1/text()
```
```xml
Pérez
Pérez
Avalón
```
##24
```xml
//carrera[@id=//alumno[estudios/asignaturas/asignatura/@codigo=//asignatura[nombre="Tecnología de los Alimentos"]/@id]/estudios/carrera/@codigo]/nombre/text()
```
```xml
I.T. Informática
```

##25
```xml
//alumno[estudios/carrera/@codigo=//carrera[not(subdirector)]/@id]/nombre/text()
```
```xml
Víctor Manuel
Luisa
Fernando
María
```

##26
```xml
//alumno[estudios/asignaturas/asignatura/@codigo=//asignatura[creditos_practicos="0"]/@id and estudios/carrera/@codigo=//carrera[nombre="I.T. Informática"]/@id]/nombre/text()
```
```xml
Víctor Manuel
```

##27
```xml
//alumno[estudios/carrera/@codigo=//carrera[plan<2002]/@id]/nombre/text()
```
```xml
Luisa
Fernando
```
