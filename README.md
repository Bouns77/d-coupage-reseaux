## Découpage symétrique

|Nom du Pole | Adresse réseau | Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage |
|:-----|:-----|:----|:-----|:-----|
|Le Pôle informatique (6 bureaux, environ 50 équipements au total) |172.16.1.0/26 |172.16.1.63 |172.16.1.1 |172.16.1.62 |
|Le Pôle développement (6 bureaux, environ 12 équipements au total) |172.16.1.64/26 |172.16.1.127 |172.16.1.65 |172.16.1.126 |
|Le Pôle Administratif (4 bureaux, environ 20 équipements au total) |172.16.1.128/26 |172.16.1.191 |172.16.1.129 |172.16.1.190 |
|Le Pôle Technicien (4 bureaux, environ 15 équipements au total) |172.16.1.192/26 |172.16.1.255 |172.16.1.193 |172.16.1.254 |

Pour les calculs j'ai pris le pole avec le plus d'équipements pour le découpage symétrique soit 50 équipement .

Grace a la table de puissance de 2 . 2^6 = 64

donc j'ai 62 adresses disponibles car 64 - 2 (adresse de reseaux , adresse de broadcast )

le CIDR = 2^5 = 32 - 6 la puissance utilisé pour le reseaux ( 2^6 ) = 26 

Donc le CIDR /26

## Découpage asymétrique

|Nom du Pole | Adresse réseau | Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage |
|:-----|:-----|:----|:-----|:-----|
|Le Pôle informatique (6 bureaux, environ 50 équipements au total) |172.16.1.O/26 |172.16.1.63 |172.16.1.1 |172.16.1.62 |
|Le Pôle Administratif (4 bureaux, environ 20 équipements au total) |172.16.1.64/27|172.16.1.95 |172.16.1.65 |172.16.1.94 |
|Le Pôle Technicien (4 bureaux, environ 15 équipements au total) |172.16.1.96/27 |172.16.1.127 |172.16.1.97 |172.16.1.126 |
|Le Pôle développement (6 bureaux, environ 12 équipements au total) |172.16.1.128/28 |172.16.1.143 |172.16.1.129 |172.16.1.142 |

Pour le pole informatique il me faut 50 adresses donc on prendra 2^6 = 64 -2 on aura donc 62 adresses . CIDR = 2^5 - 6 = 26

Pour le pole Administratif il me faut 20 adresses donc on prendra 2^5 = 32 -2 on aura donc 30 adresses . CIDR = 2^5 - 5 = 27

Pour le pole Technicien il me faut 15 adresses donc on prendra 2^5 = 32 -2 on aura donc 30 adresses . CIDR = 2^5 - 5 = 27

Pour le pole développement il me faut 12 adresses donc on prendra 2^4 = 16 -2 on aura donc 14 adresses . CIDR = 2^5 - 4 = 28
