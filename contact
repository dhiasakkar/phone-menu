import os

def ajouter():
    with open("test.txt", "a") as c:
        contact = {}
        print("**********")
        print("             Ajouter un contact                    ")
        contact["name"] = input("Nom: ")
        contact["first name"] = input("Prenom: ")
        contact["num"] = input("Numéro de téléphone: ")
        contact["adresse"] = input("Adresse: ")
        contact["email"] = input("Email: ")
        print("************")
        c.write(str(contact) + "\n")

def modif():
    with open("test.txt", "r") as c:
        contacts = c.readlines()
    
    num = input("Donner un numéro: ")
    for i, contact_str in enumerate(contacts):
        contact = eval(contact_str.strip())
        if contact["num"] == num:
            print("**********************")
            print("                   Modifier un contact              ")
            contact["name"] = input("Nouveau nom: ")
            contact["first name"] = input("Nouveau prenom: ")
            contact["num"] = input("Nouveau numéro de téléphone: ")
            contact["adresse"] = input("Nouvelle adresse: ")
            contact["email"] = input("Nouvel email: ")
            print("**********************")
            contacts[i] = str(contact) + "\n"
            break
    else:
        print("Ce contact n'existe pas.")
    
    with open("test.txt", "w") as c:
        c.writelines(contacts)

def supr():
    with open("test.txt", "r") as c:
        contacts = c.readlines()
    
    num = input("Donner un numéro: ")
    for i, contact_str in enumerate(contacts):
        contact = eval(contact_str.strip())
        if contact["num"] == num:
            print("*****************************")
            print("                Supprimer un contact              ")
            print(contact)
            if input("Pour supprimer, tapez 's': ") == "s":
                del contacts[i]
                print("Contact supprimé.")
            else:
                print("Contact non supprimé.")
            break
    else:
        print("Ce contact n'existe pas.")
    
    with open("test.txt", "w") as c:
        c.writelines(contacts)

def write_all():
    with open("test.txt", "r") as c:
        contacts = c.readlines()
    
    for contact_str in contacts:
        print(eval(contact_str.strip()))

def write():
    with open("test.txt", "r") as c:
        contacts = c.readlines()
    
    num = input("Donner un numéro: ")
    for contact_str in contacts:
        contact = eval(contact_str.strip())
        if contact["num"] == num:
            print(contact)
            break
    else:
        print("Ce contact n'existe pas.")

# Code principal
print("##############  Menu ##################")
print("1. Ajouter un contact")
print("2. Modifier un contact")
print("3. Supprimer un contact")
print("4. Afficher tous les contacts")
print("5. Afficher un contact")
print("###########################################")
choice = input("Votre choix : ")

if choice == "1":
    ajouter()
elif choice == "2":
    modif()
elif choice == "3":
    supr()
elif choice == "4":
    write_all()
elif choice == "5":
    write()
else:
    print("Choix non valide.")
