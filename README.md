# Rutas

CREAR USUARIO:

curl --location --request POST 'http://localhost:8080/usuario' \
--header 'Content-Type: application/json' \
--data-raw '{
    "nombre":"marco",
    "apellido":"perez",
    "correo":"test1@gmail.com",
    "sexo":"mujer"
    
}'

CREAR PEDIDO:

curl --location --request POST 'http://localhost:8080/pedido' \
--header 'Content-Type: application/json' \
--data-raw '{
    "userid":"630d214e892ddec8a7effc07",
    "cantidad":2,
    "precio_unitario":10000,
    "nombre_producto":"mayonesa"
}'

OBTENER PEDIDOS:

curl --location --request GET 'http://localhost:8080/getPedidos' \
--header 'Content-Type: application/json' \
--data-raw '{
    "correo":"test3@gmail.com"
}'

OBTENER USUARIOS:

curl --location --request GET 'http://localhost:8080/getUsuarios' \
--data-raw ''

ELIMINAR PEDIDO:

curl --location --request DELETE 'http://localhost:8080/deletePedido' \
--header 'Content-Type: application/json' \
--data-raw '{
    "id":"630d1e9dbe0f18457b038b40"
}'

ELIMINAR USUARIO:

curl --location --request DELETE 'http://localhost:8080/deleteUsuario' \
--header 'Content-Type: application/json' \
--data-raw '{
    "id":"630d204c5b8b4c92d06c3be7"
}'

ACTUALIZAR USUARIO:

curl --location --request PUT 'http://localhost:8080/putUsuario' \
--header 'Content-Type: application/json' \
--data-raw '{
    "id":"630d214e892ddec8a7effc07",
    "nombre":"marco",
    "apellido":"perez",
    "correo":"test1@gmail.com",
    "sexo":"mujer"

}'

ACTUALIZAR PEDIDO:

curl --location --request PUT 'http://localhost:8080/putPedido' \
--header 'Content-Type: application/json' \
--data-raw '{
    "id":"630d25e166acc72d6003e9b9",
    "cantidad":2,
    "precio_unitario":10000,
    "nombre_producto":"mayonesa"
}'
