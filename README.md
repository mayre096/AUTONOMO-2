# AUTONOMO-2






import random #Este código elige aleatoriamente una opción para la máquina en el juego

# Opciones válidas
opciones = ["piedra", "papel", "tijera"]

while True: #BUCLE PARA VOLVER A JUGAR 
    # 1. Mostrar menú
    print("\nHola, bienvenido")
    print("Seleccione una opción de juego")
    print("1 jugador")
    print("2 jugadores")
    modo = input("Ingrese la opción de juego: ")
    vidas = 3 
    while vidas > 0 
    print("el juego continua")
    vidas -= 1
    # 2. Lógica según modo de juego
    if modo == "1 jugador":
        print("Jugar contra la máquina")
        jugador1 = input("Jugador elige piedra, papel o tijera: ").lower()
        if jugador1 not in opciones:
            print("Error, elección inválida")
            continue
        jugador2 = random.choice(opciones)
        print(f"Jugador 2 (máquina) eligió: {jugador2}")

    elif modo == "2 jugadores":
        print("Jugar online con amigos")
        jugador1 = input("Jugador 1 elige piedra, papel o tijera: ").lower()
        jugador2 = input("Jugador 2 elige piedra, papel o tijera: ").lower()
        if jugador1 not in opciones or jugador2 not in opciones:
            print("Error, elección inválida")
            continue
    else:
        print("Error, volver a ingresar al juego")
        continue

    # 3. Determinar ganador
    if jugador1 == jugador2:
        print("Empate")
    elif (jugador1 == "piedra" and jugador2 == "tijera") or \
         (jugador1 == "tijera" and jugador2 == "papel") or \
         (jugador1 == "papel" and jugador2 == "piedra"):
        print("Ganador: Jugador 1")
    else:
        print("Ganador: Jugador 2")

    # 4. Fin del juego
    jugar_ahora = input("¿Nueva partida? (si/no): ").lower()
    if jugar_ahora == "si":
        print("Iniciando un nuevo juego...")
        continue #VOLVER A INICIAR EL JUEGO
    elif jugar_ahora == "no":
        print("Hasta luego, vuelve pronto")
        break #SALIR DEL JUEGO 
    else:
        print("Opción no reconocida, saliendo del juego")
        break
