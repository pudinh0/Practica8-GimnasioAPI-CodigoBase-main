1. ¿Por qué el paquete se llama adapter-mariadb si usamos MySQL?
mariaDb es un motor que es compatible con mysql, ya que comparten la misma interfaz y procotolo de red, debido a esto prisma puede utilizar cualquiera de las dos bases de datos

2. ¿Editar schema.prisma cambia algo en la base de datos antes de migrar?
no, es solo la representacion de la base de datos, si hubiera un cambio o si se necesita una nueva migracion se tiene que ejecutar el comando de prisma migrate dev.

3. ¿La carpeta de migraciones es una foto del esquema o un historial?
es un historial de las migraciones

4. ¿Por qué Horario.clase sí crea una columna y Clase.horarios no?
porque es una relación de uno a muchos, de parte de horario a clases,
esto significa que horario si tiene la columna donde sale clase, ya que este
necesita saber a que clase pertenece, a diferencia de una clase que tiene un solo horario

5. ¿De dónde sale la relación de muchos a muchos entre Miembro y Horario si nunca se declaró así?
por la tabla intermedia que es la de inscripcion, esto permite que las dos tablas se unan por medio de la
tabla inscripcion (haciendo la conexion de 1 a n de las dos a n:M)

