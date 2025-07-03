# start
#exercice1

#1)
p = 5
q = 3 * p

#2)
print( 'p vaut' , p , 'et q vaut' , q ,'; leurs somme vaut', p + q )

#3)
print( 'q est il un multiple de p')

if q%p == 0:
    print(True)
else :
    print(False)
    
#4)    
tmp = p
p = q
q = tmp

#5)
1+2+3+4+5+6+7+8+9+10/10
 
 #6)
1+2+3+4+5+6+7+8+9+10+11/11

#8)
5**4 >= 4**5

#9)
help(max)    # renvoie le plus grand


#exercice2

r = 0
m = int(input("Entrer un nombre entre 0 et 999 :"))
c = m%10
r = r*10 + c
m = m//10
print(c)
c = m%10
r = r*10 + c
m = m//10
print(c)
c = m%10
r = r*10 + c
m = m//10
print(c)
print(r)


#exercice3

def réduction(n):
    if n <10:
        return 0
    elif n >= 10 and n < 50:
        return 10
    else:
        return 20
    
assert réduction(0) == 0
assert réduction(10) == 10
assert réduction(50) == 20
assert réduction(-3) == 0
assert réduction(1000) == 20

def prix_livraison(prix):
    if 10 * prix / 100 < 5 :
        return 5
    elif 10 * prix / 100 > 100:
        return 100
    else :
        return 10 * prix / 100
    
assert prix_livraison(4) == 5
assert prix_livraison(2000) == 100
assert prix_livraison(50) == 5
assert  prix_livraison(20) == 5
assert prix_livraison(0) == 5

def facture(n,p):
    prix = n * p
    red = réduction(n)
    liv = prix_livraison(prix)
    print('prix :', prix ,'$')
    print('Reduction : ' ,- red, '%')
    print('Cout livraison : ' , liv , '$')
    print('--------------------------')
    print('Prix total (dont livraison) : ' , prix - red - liv , '$')
    
 
#correction du prof

# ## Question 3.3
# def facture(n,p):
#     prix = n*p
#     r = réduction(n)
#     l = prix_livraison(prix)
#     prix_final = prix * (1-r/100)+l
#     print("Prix :",prix,"€")
#     print("Réduction : -",r,"%")
#     print("Coût livrasion :",l,"€ ")
#     print("----------------------")
#     print("Prix total (dont livraison) :",prix_final,"€")

    
    
    
    
    
    
 #exercice4

import random

def choix_ordi():
    l= ('feuille' , 'pierre' , 'ciseaux')
    x = random.choice(l)
    
    
    choix = input('quel est ton choix humain ? ')
    if choix == 'pierre' or choix ==  'feuille' or choix == 'ciseaux':
        print('OK')
    else :
        print('Choix incorrect , je vais choisir pour toi', x)


def jeu_mourre():
    l= ('feuille' , 'pierre' , 'ciseaux')
    
    
    
    
    choix = input('quel est ton choix humain ? ')
    if choix not in l:
        print('Choix incorrect , je vais choisir pour toi', x)
        choix = random.choice(l)
        
    ch_o = random.choice(l)
        
        print('Humain =' ,choix)
        print('ordi = ' , ch_o)
        print('Vainqueur' ,vainqueur(choix,ch_o)) 

def vainqueur(choix,ch_o):
     if choix == ch_o:
              return 'égalite'
     elif(choix=='feuille ' and ch_o=='pierre') or  (choix=='pierre 'and ch_o=='ciseaux') or  (choix=='ciseaux ' and ch_o=='feuille'):
        return 'Humain Gagne'
     else :
        return 'Ordinateur Gagne'
    

# """
# # Solution 1
# 
# if choix_humain == 'pierre' and choix_ordinateur == 'pierre' :
#     print('Vainqueur : égalite')
# if choix_humain == 'pierre' and choix_ordinateur == 'feuille' :
#     print('Vainqueur : ordi')
# if choix_humain == 'pierre' and choix_ordinateur == 'ciseaux' :
#     print('Vainqueur : humain')
# # ...
# # Et on continue comme ça pour les 6 autres cas. C’est fastidieux
# # En info, il faut être paresseux et chercher à faire plus simple.
# """
# """
# # Solution 2
# 
# if choix_humain == 'feuille' :
#     if choix_ordinateur == 'pierre' :
#         print('Vainqueur : humain')
#     if choix_ordinateur == 'feuille' :
#         print('Vainqueur : égalite')
#     if choix_ordinateur == 'ciseaux' :
#         print('Vainqueur : ordi')
# 
# if choix_humain == 'ciseaux' :
#     ...
# """
# 
# # Solution 3
# 
# # Quels sont les trois cas qui font gagner l'être humain ?
# cas_gagnant_1 = (choix_humain == 'pierre'  and choix_ordinateur == 'ciseaux')
# cas_gagnant_2 = (choix_humain == 'feuille' and choix_ordinateur == 'pierre')
# cas_gagnant_3 = (choix_humain == 'ciseaux' and choix_ordinateur == 'feuille')
# 
# if choix_humain == choix_ordinateur :
#     print('Vainqueur : égalite')
# elif cas_gagnant_1 or cas_gagnant_2 or cas_gagnant_3:
#     print('Vainqueur : humain')
# else :
#     print('Vainqueur : ordinateur')
# 


#execrice5

import random



def juste_prix():
    
    n = random.randint(1,100)
    tentative = 0
    sol = int (input ('quel chiffre choissiser vous? (entre 1 et 100) '))
    
    while tentative <=7 :
       
        
    
        if sol >n :
            print(' vous etes au dessus du chiffre')
        elif sol < n:
            print(' vous etes en dessous du chiffre')
        else :
            print('Bravo vous avez gagné!')
            tentative += 1
            break

