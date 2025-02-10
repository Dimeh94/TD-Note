# TD-Note

Ex.1
Q1 :
Le format de base d'une clé RSA est de 2048 bit. Pour créer une clé au format 2096 bits il faut ajouter la précision de la taille comme suit :
openssl genrsa -out test4096.key 4096

Q2 :
Pour extraire la clé publique de la clé privée il faut executer la commande suivante :
openssl rsa -in server.key -pubout -out serveur.pub

Ex.2 :
Q1 :
Pour créer une clé protégée avec l'algorithme ds3 il faut executer la commande suivante :
openssl genrsa -des3 -out protected.key
Mon mot de passe est "Mehdi"

Q2 :
Extraction de la clé publique depuis la clé privée :
openssl rsa -in protected.key -pubout -out prot.pub
On constate que l'on doit entrer à nouveau le mot de passe pour l'extraire et que dans la clé privée le protocole qui protège la clé est indiqué avant le début de la clé 
