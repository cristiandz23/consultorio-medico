# consultorio-medico
programa para gestion de turnos, datos de pacientes y profesionales(doctores) en lenguaje C

1.- METODOLOGÍA DE TRABAJO

Construcción del TFI 2 con:

-          Programas Fuentes

-          Documentación de la forma de trabajo.

 

2.- CONFORMACIÓN DE GRUPOS

El trabajo es grupal y de hasta 4 personas (de la misma comisión).  Una vez formados los grupos, se debe informar a la cátedra los integrantes por medio de una respuesta en el foro de consultas de la materia al tema: Conformación Grupos TP 2, donde se incluirán los nombres de los integrantes y el link de acceso a los programas fuentes y documentación solicitada.

 

3.- CONSULTAS

Las consultas referentes a los enunciados de cada una de las etapas se atenderán por medio del foro y consultas por los medios habilitados (Zoom, Microsoft Teams, Telegram).  Para todo ellos, se dispondrán de horarios en los cuales los profesores atenderán las inquietudes y/o problemas de cada uno de los grupos.

4.- PAUTAS DE ENTREGA

Las entregas asociadas se realizarán exclusivamente por medio de la tarea TFI 2  AED – Segundo Trabajo Grupal, creada para tal fin en el campus virtual de la cátedra. Los archivos asociados a cada entrega deben comprimirse en un archivo ZIP o RAR nombrado bajo la estructura:

Gn-apellido1_apellido2_apellido3.zip       donde: n es el número de grupo asignado por la cátedra, seguida por los apellidos de los integrantes separados por guiones.

Cada entrega la realizará sólo uno de los integrantes del grupo, indicando claramente en un documento llamado integrantes.txt (contenido dentro del archivo comprimido) el nombre de cada uno de los integrantes y su email.

 

5.- DOCUMENTACIÓN A ENTREGAR

Deberán entregar a través de la tarea los siguientes archivos dentro del zip:

Integrantes.txt: archivo de texto que contendrá el apellido, nombre y correo electrónico de cada uno de los integrantes del grupo.
Los  programas C++ (.cpp, .h) con su respectivo archivo ejecutable (.exe), ya que cada módulo deberá implementarse en un programa independiente. Los archivos deberán tener el nombre del programa implementado. Ejemplo: CentroMedico.cpp y CentroMedico.exe
Informe.doc: documentación con el análisis del enunciado de los módulos, decisiones de diseño y los casos de prueba correspondientes a cada uno.
 

Aclaración Importante: los archivos que se entreguen en la sección del campus habilitada para tal fin deben ser reflejo del repositorio usado durante todo el proceso de desarrollo.

 

VALIDACIONES E INTERACCIÓN

La aplicación debe solicitar en todo momento el ingreso de información de forma clara y consistente.

La interacción con el usuario debe ser lo más amigable posible (mensajes de información y/o de error específicos, limpieza de pantalla, etc.). Se deben implementar todas las validaciones que se consideren necesarias (además de las enunciadas en este documento).

Fecha máxima de entrega: 23/02/2024

 

Implementación de Módulos

Módulo Consultorios:

Esta parte del proyecto estará dirigida a los diferentes profesionales de la salud que atienden y registran la Historia Clínica de sus pacientes en una base de datos. El sistema deberá contar con un listado de los pacientes que están registrados para ser atendidos en ese día, para visualizarla, el profesional deberá identificarse en el sistema por medio de su “Nombre de Usuario” y “Contraseña” y accediendo a la opción indicada. De esta manera el Profesional llamará por apellido y nombre al paciente que atenderá, una vez realizada esta tarea procede al ingreso de la historia clínica, en un texto de no más de 380 caracteres. Luego de realizada esta operación del sistema, el paciente debe desaparecer del listado de pendientes para ser atendidos.

Los datos del paciente que necesita un profesional de la salud en este proceso son: Apellido y Nombres, DNI, Domicilio, Edad (calculada con la fecha de nacimiento registrada), Peso, Talla.

La historia clínica  es común para todos los profesionales del centro médico, por lo tanto, se deberá visualizar fecha de atención de la misma y el nombre del profesional que lo atendió.

 

Módulo Recepción:

Este módulo satisface las necesidades del personal que recibe al paciente. Desde aquí se realiza  ingreso de los pacientes (alta de un nuevo paciente), y la registración de los turnos (Esto solo lo realizan los recepcionistas).Esta aplicación debe permitir obtener un informe de los pacientes atendidos en determinada fecha por un determinado profesional de la salud.

 

Módulo Administración:

             Esta área del centro médico es la encargada de realizar la generación de los nuevos profesionales de la salud que trabajan en el establecimiento, así como también de los empleados recepcionistas que realizan la registración de los turnos y pacientes. Deberá poder visualizar las atenciones realizadas por los profesionales de la salud según el mes en curso, en este punto se debe obtener un listado u informe que indique por profesional cuantas atenciones realizo en el mes actual.

                Para incentivar a los Profesionales, la administración otorga un bono mensual al que haya registrado la mayor cantidad de turnos en ese periodo, por lo tanto, una necesidad del sistema, es indicar cual es el profesional que debe recibir el bono.

 

I. INTERFAZ DE USUARIO

El diseño visual de la interfaz es libre y se pueden utilizar elementos gráficos (logos, colores) para hacer las pantallas de la aplicación más atractivas. Por ejemplo, utilizar símbolos o íconos para representar las especialidades de los profesionales, las pantallas de los informes, etc.  Opcionalmente, se le podrá dar un nombre y proponer un logo que represente a la aplicación y utilizarlo en las pantallas.

 

Al ingresar a la aplicación, se presenta el Menú Principal, donde el usuario debe tener una cuenta creada para poder iniciar una sesión. A continuación, se muestra el esquema de opciones que debe respetar el menú principal:

              Modulo Consultorios

              =========================

              1.- Iniciar Sesión

              2.- Visualizar Lista de Espera de Turnos (informe)

              3.- Registrar Historia Clínica

              4.- Cerrar la aplicación.

 

              Ingrese una opción: _

 

 

 

              Modulo del recepcionista

              =========================

              1.- Iniciar Sesión

              2.- Registrar Pacientes

              3.- Registrar Turno

              4.- Listado de Atenciones por Profesional y Fecha

              5.- Cerrar la aplicación.

 

              Ingrese una opción: _

 

 

 

 

 

              Módulo Administración

              =========================

              1.- Registrar Profesionales

              2.- Registrar Usuario Recepcionista

              3.- Atenciones por Profesional

              5.- Ranking de Profesionales por Atenciones

              6.- Cerrar la aplicación.

 

              Ingrese una opción: _

 

 

 

II. GESTIÓN Y AUTENTICACIÓN DE USUARIOS

Dentro del módulo administración, el usuario tendrá la posibilidad de crear un nuevo Profesional y la opción de crear un nuevo Recepcionista. Para esto el programa le solicitará las credenciales para validar y verificar el nombre de usuario y la contraseña.

 

Nombre de usuario: Quedará definido por una cantidad mínima de 6 caracteres y máxima de 10, los cuales podrán ser letras, números y/o símbolos del conjunto {+,-,/,*,?,¿,!,¡}. Deberá cumplir con los siguientes requisitos:

Ser único para cada usuario registrado.
Comenzar con una letra minúscula.
Tener al menos 2 letras mayúsculas.
Tener como máximo 3 dígitos.
 

Ejemplos de nombres de usuario incorrectos: AbC123 (no cumple con b), pTS!1234 (no cumple con d), g178Mci (no cumple con c), mARtin123gomez (tiene mas de 10 caracteres).

 

Ejemplos de nombres de usuario correctos: mARtin12, jo97!AR.

 

Contraseña:  Su conformación no podrá darse al azar, sino que deberá respetar lo siguiente:

 

Deberá contener al menos una letra mayúscula, una letra minúscula y un número.
No podrá contener ningún carácter de puntuación, ni acentos, ni espacios. Sólo caracteres alfanuméricos.
Deberá tener entre 6 y 32 caracteres.
No debe tener más de 3 caracteres numéricos consecutivos.
No debe tener 2 caracteres consecutivos que refieran a letras alfabéticamente consecutivas (ascendentemente). Este criterio es válido tanto para letras mayúsculas, minúsculas o combinación de ambas.
 

Ejemplos de contraseñas mal formadas: Ach32 (no cumple con c), dorit1234 (no cumple la regla a ni la d), sA;gotAP.10 (no cumple con b), aBuel123 (no cumple con e).

 

Ejemplo de contraseñas bien formadas: Achus32, 125Af89, aLejo123, DORItO45, 4aC2sa.

 

Nota: Tanto en el nombre de usuario como en la contraseña deben distinguirse mayúsculas y minúsculas.

 

III. ARCHIVOS

Para no perder la información entre ejecuciones, es necesario mantener los datos de las cuentas de usuario registradas.  Para cumplir con este objetivo deberá implementarse la persistencia de la información manejando archivos que se describirán más adelante en este apartado.  La estrategia sugerida para cumplir con este objetivo es:

 

Cuando se inicia la aplicación, se cargan los datos en estructuras de datos en memoria.
Durante la ejecución de la aplicación se actualizan estas estructuras.
Al terminar cada sesión se agrega el contenido de la misma al archivo correspondiente.
 

Los datos de las cuentas de usuario se almacenarán en los archivos Recepcionistas.dat y Profesionales.dat. Estos archivos serán de formato binario y guardarán variables diseñadas en una estructura de datos a fin de representar la información asociada a las cuentas de usuarios (es decir, nombre y contraseña). Cada vez que se inicie la aplicación, se utilizará la información almacenada en este archivo para validar el inicio de sesión y/o la creación de un nuevo usuario.

 

Cada vez que un usuario cree un registro de Pacientes el mismo se guardará dentro del archivo Pacientes.dat y los turnos correspondientes dentro del archivo Turnos.dat. Se sugiere utilizar el siguiente diseño tanto para los archivos mencionados, como para las estructuras en memoria que donde se registran los procesos descritos:

 

Usuarios:

Usuario              char [10]
Contraseña           char [10]
Apellido y Nombre    char [60]

 


Profesionales:

Apellido y Nombre    char [60]
IdProfesional        Int 
Dni                  Int
Teléfono             char[25]

 

Pacientes:                 

Apellido y Nombre    char [60]
Domicilio            char [60]
DniPaciente          int
Localidad            char [60]
FechadeNacimiento    Fecha
Teléfono             char[25]


 

Turnos:

IdProfesional        int
Fecha                fecha
DniPaciente          int
DetalledeAtención    char[380]

 

 

 

III. ADICIONALES

Deberá implementar las operaciones de Archivo Binario Alta, Baja (Lógica)  y Modificación utilizando:

 

Una Estructura de datos dinámica del tipo PILA con el Archivo Usuarios.dat, como lista enlazada donde cada nodo contiene un registro y un puntero al siguiente nodo.
Una Estructura de datos Jerárquica no lineal del tipo Árbol Binario con el Archivo Profesionales.dat.
 
