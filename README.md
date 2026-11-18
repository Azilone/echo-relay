# echo-relay

Page de retour de connexion (OAuth) pour l'assistant vocal Echo.

Les services en ligne (Notion, Linear…) n'acceptent comme adresse de retour que HTTPS. L'Echo est sur le réseau
local en `http://` : cette page reçoit le retour et renvoie aussitôt le navigateur vers l'adresse locale de l'Echo
(cachée dans le paramètre `state`). Aucun serveur, aucun secret : le code reste dans le navigateur, et seules les
adresses locales (réseau privé, `.local`, `localhost`) sont acceptées.
