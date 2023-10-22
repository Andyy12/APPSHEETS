CONCATENATE
(
    "¡Hola "
    ,LOOKUP(USEREMAIL(), "USERS", "USEREMAIL", "NOMBRE CORTO")
    ,"! "
    ,IF
    (
       AND([BienvenidaHoraActual] >= 1, [BienvenidaHoraActual] < 12)
       ,"Buenos días"
       ,IF
       (
          AND([BienvenidaHoraActual] >= 12, [BienvenidaHoraActual] < 18)
          ,"Buenas tardes"
          ,"Buenas noches"
       )
    )
)
