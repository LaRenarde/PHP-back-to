# Etre ou ne pas être connecté...

## Construction d'un formulaire de connexion
Dans un fichier <i>index.php</i>, construisez un formulaire de connexion comprenant 2 champs : login et pwd.<br>
Ce formulaire renvoie vers un script <i>connexion.php</i>.<br>

## Validation du formulaire
En cas de connexion réussie, on mettra les identifiants (credentials) en session ($_SESSION).<br>
Dans tous les cas, on effectuera une redirection vers <i>index.php</i>.<br>

## Gestion de la connexion
Dans index.php, on incluera une page <i>page.php</i> lorsque l'utilisateur sera connecté.<br>Sinon, on affichera le formulaire de connexion.<br>Du coup, on peut imaginer que ce formulaire soit dans un fichier séparé <i>form.php</i>.
On aura dans la page <i>page.php</i> un bouton (lien) de déconnexion, renvoyant vers un script <i>logout.php</i> qui, une fois la session détruite, renverra vers <i>index.php</i>.

## Une table users
Si vous ne l'avez déjà fait, créez une base de données contenant une table users avec les champs correspondant au formulaire de connexion.<br>
Adaptez le processus de connexion en conséquence ( requête préparée ;-) ).<br>

## Mais c'est quoi une session ?
C'est <a href='https://www.grafikart.fr/tutoriels/php/session-start-825' target="_blank">ça</a>.
Observez la présence du cookie PHPSESSID dès lors que vous faites un session_start() dans votre script Php.<br>

# Etre connecté et le rester
Dans votre formulaire de connexion, ajoutez un champ de type checkbox intitulé "Rester connecté" ou "Se souvenir de moi". N'oubliez pas l'attribut name ;-).<br>
Voici le fonctionnement attendu :<br>
- Lorsque l'on valide le formulaire et que l'utilisateur est reconnu, si la case "Rester connecté" était cochée, alors il faut créer un cookie (créer une fonction pour ça). Appelez-le "auth" par exemple.<br>
- Si une session existe, on n'affiche pas le formulaire.<br>
- Si aucune session n'existe mais qu'un cookie "auth" ($_COOKIE) est présent (dans la requête du navigateur), vérifier si la valeur du cookie "auth" est bien celle attendue (grâce à la fonction qui a servi à générer le cookie), et connecter l'utilisateur ($_SESSION).

Pour un aperçu complet, vous pouvez regarder <a href='https://www.grafikart.fr/tutoriels/php/cookie-php-souvenir-412' target="_blank">ici</a>.

