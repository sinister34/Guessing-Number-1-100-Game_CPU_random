# Guessing-Number-1-100-Game_CPU_random
Simple Number Estimation Game with Points (Turkish)
import random
def main():
    name = input("Adınız: ")
    number = random.randrange(0, 101)
    score = 100
    while True:

        guess = int(input("1 ile 100 arası bir sayı tutunuz ve tahmininizi yazınız: "))


        if guess > number:
            print("Tahmininiz çok BÜYÜK")
            score = score - 1
        elif guess < number:
            print("Tahmininiz çok KÜÇÜK")
            score = score - 1
        elif guess == number:
            print("Tebrikler, doğru bildiniz!")
            break



    if score < 0:
        score = 0

    print("puanınız " + str(score))
main()



choice = 'e'
scores = []

while True:

    choice = input ("Tekrar oynamak ister misiniz? Devam etmek için e ye basınız")
    choice.lower()
    if choice== "e":
        main()

    else:
        break
