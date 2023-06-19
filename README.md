# BD-P3-RESPUESTAS-TEORIA
ITEM 1: Defina clave primaria y foránea
  CLAVE PRIMERIA: Es uno o mas atributos que permiten identificar univocamente un registro dentro de una relacion
  CLAVE FORANEA: Se utiliza para referenciar un registro unico dentro de otra relacion en la cual dicha CF es su CP
ITEM 2: Responda y justifique las siguientes preguntas:
  *¿Qué es una tupla? Compare con una tabla
    cada tupla se considera como un conjunto de pares(atributo, valor)
  *¿Las tuplas de una relación tienen un orden específico? Compare con una tabla.
    las tuplas de una relacion no estan ordenadas
  *¿Puede una relación carecer de clave primaria? Justifique.
    En una relacion no pueden haber tuplas repetidas, de ahi se desprende que siempre existira una clave primaria para toda relacion
  *¿Puede una relación carecer de clave foránea? Justifique.
    Si puede carecer de clave foranea, una relacion puede no tener una clave foranea que haga referencia a otra relacion
  *¿Una clave foránea puede contener valores nulos? Justifique.
    Si, dependiendo de las restricciones y de como este definido el modelo relacional una clave foranea dentro de una relacion puede contener valores nulos
  *Enuncie la Propiedad de Clausura, e indique las consecuencias que de ella se desprenden
    Todo operador del algebra toma como argumento/s esquemas de relaciones y devuelve tambien un esquema de relacion
    CONSECUENCIAS: _Ninguna expresion del algebra puede generar tuplas repetidas
                   _Generar expresiones encadenadas o anidadas
ITEM 3:
*Especifique dos relaciones con las siguientes características:
  *Una relación que posea una clave foránea (que no forme parte de la clave primaria de dicha relación) y la otra,
   que sea referenciada por la anterior. Identifique claves primarias y foráneas.
    Una persona puede inscribirse en una universidad
    Persona= {dni,nom,idu} CP: dni, CF: idu
    Universidad= {idu,nom} CP: idu
  *La clave foránea de la primera, ¿puede contener nulos? Justifique
    En este caso, si, ya que no hay una regla general dentro del modelo relacional que diga que no puede contener nulos, por lo tanto si puede contener nulos,
    la que no tiene que tener nulos es la clave primaria dni
    que pueda o no contener nulos dependera de que nosotros los diseñadores digamos en que si o no esta permitido que una persona este inscripta en alguna universidad
  *¿Tienen igual nombre la primaria y la foránea vinculadas? ¿sería conveniente que tengan igual nombre?
    En este caso si tienen el mismo nombre, no necesariamente tiene que ser asi, pero es conveniente pienso para a la hora de hacer una consulta que coincidan los nombres
  *¿debieran pertenecer al mismo dominio?
    Si, es uno de los requisitos que satisfacen que ese atributo sea clave primeria, la CF de la relacion referenciante debe tener el mismo dominio que los atributos de la CP de la relacion referenciada
*Especifique dos relaciones con las siguientes características:
  *Una relación que posea una clave foránea (que forme parte de la clave primaria de dicha relación) y la otra,
   que sea referenciada por la anterior. Identifique las claves primarias y foráneas.
    Ciudad= {nomc,idp,superf} CP: nomc + idp,  CF: idp
    Pais= {idp,nomp} CP: idp
  *La clave foránea de la primera, ¿puede contener nulos? Justifique
    En este caso no, porque dicha foranea forma parte de la CP de Ciudad, no es por la restriccion de la foranea en si, sino porque forma parte de la CP
