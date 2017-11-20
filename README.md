
"informacion" : informacion segun nuestro proyecto

--CREA UNA LISTA DE COMANDOS---
Router(config)#kron policy-list "NombreLista"
Router(config-kron-policy)#cli sh run | redirect tftp://"IP-TFTP-SERVER"/"nombre-archivo".cfg
Router(config-kron-policy)#exit

---USA LA LISTA DE COMANDO DIARIAMENTE A LAS 11:59---
Router(config)#kron occurrence "Nombre-ocurrance" at 23:59 recurring
Router(config-kron-occurrence)#policy-list "NombreLista"
