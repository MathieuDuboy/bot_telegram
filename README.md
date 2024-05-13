## 1- Créer le Bot via @BotFather

Rendez-vous sur : 
[https://web.telegram.org/k/#@BotFather](https://web.telegram.org/k/#@BotFather)

Crééz un bot en tapant
 ```
/newbot
```
Suivez les instruction et ajoutez un nom de bot : par exemple pour le premier bot que vous allez créér :
 ```
novabot_1
 ```
et un nom d'utilisateur (doit terminer par "bot" : Par exemple ici (vous pouvez mettre n'importe quoi):
 ```
novabotuser1bot
 ```
BotFather va alors vous répondre que le bot que vous venez de créer a été fabriqué et vous donnera un token  (à conserver)
```
6582606880:AAER2ogFrXdnuLLHjy4zD1ZQdddfomQ_xxx
```


## Création du WebHook

Connectez vous via Filezilla au FTP du domaine (identifiants FTP sur Hostinger) et dans le dossier /bot_telegram
dupliquez le fichier webhook_0.php en webhook_1.php pour votre premier bot (webhook_2 pour le deuxième et ainsi de suite).

Modifiez la ligne 8 à 16 avec les infos suivantes :
```bash
// ******************************************************************* //
//********** INFOS A MODIFIER (dédiée au bot particulier ) *********** //
// ******************************************************************* //
$log_file_number = 0; // cet exemple est 0, le premier BOT sera le numero 1
$token_bot =  ''; // remplacer ici par un truc comme : 7022872810:AAHQWOgMf0JJigxbaiH_XdJ-Zj0-xxxxxxxxx
$robot_name = ''; // Exemple : Bot de Michel Martin
// Ceci peut etre modifié à votre guise !
$from_name = 'NovaBTC BOT';
$to = 'simon@novabtc.io';
```

## Enregistrement du WebHook sur le bot 
Une fois que le bot est créé sur BotFather et que le fichier webhook_XX.php est créé, il va vous falloir enregistrer le webhook sur le bot via Télégram.

Rendez vous sur l'url :


```
https://api.telegram.org/bot<token>/setwebhook?url=https://novaregistrationbot.online/bot_telegram/webhook_<numero du bot>.php
```
Remplacez ici <token> par votre vrai token du bot

Remplacez ici <numero du bot> par 1, 2, 3 ou le chiffre de votre bot que vous venez de créer. Ici c'est à l'infini que vous pouvez dupliquer les webhook et les numeros.


