import random
import Palavras

palavra = random.choice(Palavras.palavras) 
letras = set(palavra)
alfabeto = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
letras_da_palavra = set(palavra.upper())
letras_usadas = set()
vidas = 6

def mostrar_palavra_oculta(palavra, letras_usadas):
    oculta = ""
    for letra in palavra:
        if letra.upper() in letras_usadas:
            oculta += letra + " "
        else:
            oculta += "_ "
    return oculta

def forca():
    vidas = 6
    print("Bem vindo ao jogo da forca! \nVocê tem 6 vidas, a cada erro perderá uma.\nBoa sorte!")
    print("--------------------------------------------------------")
    while len(letras_da_palavra) > 0 and (vidas > 0):
        print("Essas são as letras já usadas: ", " ".join(letras_usadas))
        print("Essa é a palavra que temos até o momento: ", mostrar_palavra_oculta(palavra, letras_usadas))
        print("--------------------------------------------------------")
        letraDigitada = input("Digite uma letra: ").upper()
        if letraDigitada in alfabeto:
            if letraDigitada in letras_usadas:
                print("Você já usou essa letra.")
            elif letraDigitada in letras_da_palavra:
                print("---------------------------------")
                print("Parabéns, você acertou a letra.")
                print("---------------------------------")
                letras_usadas.add(letraDigitada)
                letras_da_palavra.remove(letraDigitada)
            elif letraDigitada not in letras_da_palavra:
                print("---------------------------------------------")
                print("Infelizmente essa letra não está na palavra. ")
                print("---------------------------------------------")
                letras_usadas.add(letraDigitada)
                vidas-= 1
        elif letraDigitada not in alfabeto:
            print("-----------------------------------------------------")
            print("Erro ao computar o caractere, favor tentar novamente.")
            print("-----------------------------------------------------")
    if vidas > 0:
        print("Você acertou a palavra %s." %palavra.upper())
        print("---------------------------------------------")
    else:
        print("Suas vidas acabaram :c \nA palavra era: %s." %palavra.upper())
        print("---------------------------------------------")
    jogar_novamente = input("Deseja jogar novamente? (S/N): ").upper()
    if jogar_novamente == 'S':
        forca() 
    else:
        print("Obrigado por jogar!")

forca()
        
        

        






