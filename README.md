# BlackJack

Mi dirección de github de este repositorio es el siguiente: [Github](https://github.com/FedeOcejo/BlackJack.git)

Ge creado un código que simula el famoso juego de casino Black Jack mediante listas 

El diagrama de flujo de este código es:
![diagrama de flujo Black Jack](https://github.com/FedeOcejo/BlackJack/blob/main/Flowchart_BlackJack.png)

```from random import choice, sample
 
cartas = {
   chr(0x1f0a1): 11,
   chr(0x1f0a2): 2,
   chr(0x1f0a3): 3,
   chr(0x1f0a4): 4,
   chr(0x1f0a5): 5,
   chr(0x1f0a6): 6,
   chr(0x1f0a7): 7,
   chr(0x1f0a8): 8,
   chr(0x1f0a9): 9,
   chr(0x1f0aa): 10,
   chr(0x1f0ab): 10,
   chr(0x1f0ad): 10,
   chr(0x1f0ae): 10,
}
 
print("cartas: {}".format(" ".join(cartas. keys())))
print("puntos: {}".format(list(cartas.values())))
 
print("1\ Interacción estánar sobre un diccionario")
for carta, valor in cartas.items ():
     print ("la carta {} vale {}" .format(carta, valor))
 
print("2\ interación ordenada sobre un diccionador rio")
for carta in sorted (cartas.keys ()):
   print ("la carta {} vale {}" .format(carta, cartas[carta]))
 
print("3\ Black Jack")
lista_cartas = list (cartas)
 
print("Ha seleccionado:", end= " ")
carta= choice(lista_cartas)
score = cartas [carta]
print(carta, end=" ")
carta = choice (lista_cartas)
score += cartas[carta]
print(carta,end=" ")
print(" >>> su puntuación es de", score)
 
main_banca = sample(lista_cartas, 2)
score_banca = sum(cartas[carta] for carta in main_banca)
print ("La banca tiene: {} {} >> su score es {}".format (main_banca[0],
                                                           main_banca[1],
                                                           score_banca))
 
def juego():
       if score_banca > score :
           print ("banca ha ganado")
       elif score > score_banca :
           print ("Has ganado")
       elif score == 21:
           print ("Black Jack")
juego()
