# Exo-Distributed-Ledger-Technology

#### 1. Un arbre de merkle nécessite une paire de hashes pour produire un nouveau hash parent. Il faut donc a absolument que le nombre de transactions qui produiront le Merkle root soit pair. Comment est géré le cas ou le nombre de transactions dans le Block à valider est impair pour générer un Merlke root ?
&nbsp;
* Si le nombre de transactions est impair, le dernier nœud est dupliqué. Il est hashé avec lui-même afin de produire le hash parent.  
&nbsp;
#### 2. Dans le réseau bitcoin, Comment un nouveau noeud arrive t'il à retrouver ses pairs et ainsi rejoindre le réseau ? Expliquer le processus avec vos propres mots.
&nbsp;
* Lorsque qu'un noeud crée une connection sortante il transmet dans un premier temps sa version de protocole de communication. Un noeud distant répond en retour avec sa version de protocole. Une fois les versions de protocole echangées et acceptées entre paires(noeud), la communication entre noeud est en mesure d'être établie.
La connexion distante retourne un paquet de données nommé 'verack' confirmant l'acceptation de la version de protocole du noeud emetteur pour valider l'autorisation de communication.
&nbsp;
#### 3. Pouvez vous nommer au moins une personne qui a ou aurait pu influencer directement ou indirectement la création de Bitcoin par ses travaux (une personne qui n'a pas été nommée dans le cours)?
&nbsp;
* Nick Szabo est un informaticien, juriste et cryptographe connu pour ses travaux de recherche sur les contrats numériques et la monnaie numérique.
En 1998, Szabo a conçu un mécanisme de monnaie numérique décentralisée qu'il a appelé « Bit gold »8,9 (en français « Or de bits »). Bit gold n'ayant pas reçu suffisamment de soutien, il n'a jamais été implémenté, mais a été désigné comme « précurseur direct à l'architecture
&nbsp;
#### 4. Avec vos propres recherches et grâce aux compétences acquises en cours pouvez vous expliquer comment une Blockchain crée un lien entre ses différents Blocks?
&nbsp;
* Chaque nouveau block est lié au précédent par le hash de son header. Pour créer un nouveau block dans la blockchain, un lien doit être établit entre le hash du block précédent et ce nouveau bloc. Chaque nouveau block crée un lien avec le précédent par le hash de son header.
&nbsp;
#### 5. Quelle structure de données informatique peut représenter le mieux cette chaine de Block: https://en.wikipedia.org/wiki/List_of_data_structures ?
&nbsp;
* La structure de données informatique représentatn le mieux la blockchain est la 'Hash-based structures'.
&nbsp;
#### 6. Si je souhaite modifier une transaction de 10 bitcoin que j'ai effectué il y a 6 mois en une transaction de 1 Bitcoin, que dois je modifier dans la Blockchain et que dois je mettre en oeuvre pour que cette modification persiste ? Est ce possible selon vous ?
&nbsp;
* Pour réécrire une transaction réalisée dans la blockchain, il est necessaire  de  recalculer tout les hashs de tous les blocks regroupant les transactions émises durant les 6 derniers mois. Le hash du dernier block est unique et est modifié si une transaction est modifiée dans la blockchain.
Et pour valider cette nouvelle blockchain avec sont dernier block jusqu'à la dernière transaction : 
il faudrait que ce dernier block soit réécrit avant qu'un noeud valide un nouveau block avec de nouvelles transactions.
Compte tenu de la puissance nécessaire pour valider 'the proof of work' pour l'ensemble des hashs des blocks émis depuis 6 mois cela parait impossible.
