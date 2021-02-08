# Créer un formulaire d'inscription
Créez un formulaire d'inscription avec les champs login et pwd.

## Validation
Créez un script de validation (Php) des données saisies (on ne fera pas de validation côté navigateur ici) :<br>
<ul>
    <li>Le champ login sera une adresse email. Elle ne devra pas être déjà présente dans la base de données.</li>
    <li>Le champ pwd devra comporter au minimum 6 caractères dont au moins 1 majuscule et un caractère spécial.</li>
    <li>Il faudra traiter les valeurs des champs de manière à éviter une injection Sql (prepare) et une injection de code Javascript.</li>
</ul>
Vous trouverez des informations <a href="https://www.w3schools.com/php/php_forms.asp">ici</a> par exemple.<br>

# Validation par mail
Implémentez un sytème de validation par mail. Vous pouvez vous inspirer de <a href="https://m-gut.developpez.com/tutoriels/php/mail-confirmation/">ceci</a>.

# Tests
Testez votre système avec votre formulaire de connexion.
