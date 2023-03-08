# Prueba-basada-en-men-de-pedidos
Esta prueba consistía en un menú para pedidos de sushi.


#creacion  menú
from re import X


sw= 1
sw1=1
sw2=1
rut=[]#rut de cliente registrado
nombre=[]#nombre de cliente registrado
direccion=[]#direccion de cliente registrado
comuna=[]#comuna de cliente registrado
correo=[]#correo de cliente registrado
edad=[]#edad de cliente registrado
celular=[]#celular de cliente registrado
tipo=[]#tipo de cliente registrado
pedidos=[]#tipo de pedido de la gente
nombrepedidos=[]#nombre de cada pedido
subtotal=0#subtotal de pedido
preciocalifornia=0#precio del total de california
preciocrab=0 #precio total de crab humano
preciotempura=0#precio total de tempura tuna nikkei
while sw==1:
    print("entrando al menú")
    menuprincipal=int(input("------ Bienvenido a Sushi-Nikkey ------ \n que opción desea escoger. \n 1. ----> Registro de cliente. \n 2. ----> consultar datos de cliente. \n 3. ----> registro de pedido. \n 4. ----> salir. \n "))
    if menuprincipal>0 and menuprincipal<5:
        if menuprincipal==1:
            while sw1==1:
                print("a escogido registro de cliente.")
                run=int(input("registre su rut sin coma ni guion por favor. \n"))
                if run >50000000 or run < 9999999999:
                 print("registro de rut exitoso. \n")
                else:
                    print("ingrese un rut valido. \n")
                rut.append(run)
                nombrecliente=str(input("escriba su nombre completo.\n"))
                nombre.append(nombrecliente)
                print("nombre registrado con exito.")
                direccioncliente=str(input("escriba su dirección. \n"))
                direccion.append(direccioncliente)
                print("direccion registrada con exito. \n")
                comunacliente=str(input("escriba su comuna.\n"))
                comuna.append(comunacliente)
                correocliente=str(input("ingrese su correo. \n"))
                correo.append(correocliente)
                edadcliente=int(input("ingrese su edad. \n"))
                if edadcliente== 18 or edadcliente > 18:
                    print("edad registrada con exito. \n")
                else:
                    print("registro valido solamente para gente de igua o mayor a 18 años. \n")
                edad.append(edadcliente)
                celularcliente=str(input("ingrese su número de telefono. \n"))
                celular.append(celularcliente)
                print("numero de celular registrado con exito. \n")
                tipocliente=str(input("¿cuantas veces compraria en este local?. solamente ocupar palabras: preferencial, habitual y ocasional. \n"))
                tipo.append(tipocliente) 
                print("registro de cliente con exito")
                sw1= 0
        if menuprincipal ==2:
            consulta_r=int(input("ingrese rut de usuario"))
            print("espere un momento")
            if consulta_r==rut[0]:
                print(f"rut de cliente: {rut[0]}")
                print(f"nombre de cliente: {nombre[0]}")
                print(f"direccion: {direccion[0]}")
                print(f"comuna de cliente: {comuna[0]}")
                print(f"correo de cliente: {correo[0]}")
                print(f"edad de cliente: {edad[0]}")
                print(f"celular de cliente: {celular[0]}")
                print(f"tipo de cliente: {tipo[0]}")

        if menuprincipal ==3:
            sw2=1
            print("bienvenido al registro de pedido. \n")
            cantidadcalifornia=int(input("¿cuanta cantidad de california le gustaria pedir?\n"))
            preciocalifornia=cantidadcalifornia*5100
            subtotal= subtotal=+preciocalifornia
            print(f"usted pidio {cantidadcalifornia} porciones de california")
            cantidadcrab=int(input("¿cuanta cantidad de crab humano le gustaria pedir? \n"))
            preciocrab=cantidadcrab*6200
            subtotal = subtotal=+preciocrab
            print(f"usted pidio {cantidadcrab} porciones de crab humano.")
            cantidadtempura=int(input("¿cuanta cantidad de tempura tuna nikkei le gustaria pedir? \n"))
            preciotempura=cantidadtempura*5800
            subtotal=subtotal=+preciotempura
            print(f"usted pidio {cantidadtempura} porciones de tempura.")
            total=total=+subtotal
            print(f"usted tiene un total de ${total}")
            dinero=int(input("¿con cuanto dinero le gustaria pagar?. \n"))
            if total==dinero:
                print("pago con el mismo valor del total. no recibe vuelto.")
            if total>dinero:
                print("dinero insuficiente.")
            if total<dinero:
                vuelto=dinero-total
                print(f"su compra fue exitosa, este es su vuelto ${vuelto}.")
        if menuprincipal==4:
            continu=int(input("¿Usted desea salir de Sushi-nikkey? \n 1. si \n 2. no\n"))
            if continu==1:
                print("Gracias por preferir sushi-nikkey. Adios!")
                sw=0
            else:
                sw=1
