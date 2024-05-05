# grep


| rechercher  | remplacer |
| ------------- | ------------- |
|Espace fine pour tous les signes de ponctuation doubles|
| `<div>(?<=\w)(( \| )*?)([?!;:])</div>` |`<div>~<$3</div>`|
|Espaces fines pour les guillemets Français|
|`(«\s*)(.*?)(\s*»)`|`«~<$2~<»`|
|Plusieurs espaces par une seule|
|`[~m~>~f~\|~S~s~<~/~.~3~4~% ]{2,}`|	`\s`|
|Suppression des espaces de fin|
|`\s+$`|			
|Repère les ordinaux « er », « e » après un chiffre|
|`(?<=\d)r?e[rs]*\>`	|	`un style particulier`|
|Repère les exposants pour les siècles|
|`(?i)\<(X\|I\|V)+\K(er\|e)s?\>`	|	`un style particulier`|
|Trois points (ou plus) consécutifs en ellipse|
|`\.{3,}`		|				`…`|
|Apostrophes|
|`\w\K\x{02BC}(?=\w)`		|		`~’`|
|Attraper ce qui est entre des parenthèses (avec et sans inclure les parenthèses)|
|sans : `\([^)]+\)` & avec : `(?<=\()[^)]+`|

 


