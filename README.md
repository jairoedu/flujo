import random
nombre=input("¿como te llamas?: ")

print(f"vienvenido {nombre} " ,"es hora de jugar al ahorcado:")

input("¡estas listo?:  ")

input("exelente comencemos  ")

palabras=['raton','carton','carbon','canton']
adivina_la_palabra=random.choice(palabras)
estado_ahorcado=['_']*len(adivina_la_palabra)
intentos=6
while intentos>0 and '_'in estado_ahorcado:
    print(''.join(estado_ahorcado))
    letra_usuario=input('introduce una letra: ').lower()
    if letra_usuario in adivina_la_palabra:
        for c in range(len(adivina_la_palabra)):
            if adivina_la_palabra[c]==letra_usuario:
                estado_ahorcado[c]=letra_usuario
            else:
                intentos-=1
                print(f'¡correcto! te quedan {intentos}intentos.')
                
   
        
