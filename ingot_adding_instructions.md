AJOUT D'UN LINGOT POUR LE MODPACK "Infinite Cadriz":
====================================================

Si tu veux proposer des lingots à rajouter au modpack `Infinite Cadriz`, envoie ton fichier compressé au format `zip` ou `tar` qui est le compressé du dossier `<lingot_id>` avec:

### CONTENUS

1 Fichier texte et 1 à 5 Fichier(s) image(s) :

- `<lingot_id>.json` sur la base de [`ingot_template.json`](./ingot_template.json):
	- Minecraft:
		- `#/hasDust` si le lingot a une forme en poudre
		- `#/hasBlock` si le lingot a une forme en bloc
		- `#/crafting/smelting` est à mettre sur `-1.0` si:
			1) `#/hasDust` est *false*
			2) ou pour désactiver le four.  
			Cela correspond à l'xp gagné.
		- `#/crafting/compress` et `#/crafting/uncompress` doivent être à `{"type": "none"}` si `#/hasBlock` est *false* ou pour enveler le craft.  
			Sinon mettre `crafting_shaped` ou `crafting_shapeless` avec le contenu json tel qu'une recette Minecraft Vanilla,  
			sans `#/result` mais le `#/result/count` est déplacé dans `#/crafting/(un)compress/amount`.
	- "Ex Nihilo: Creatio":
		- `#/exnihilocreatio/addItems` Ajouter les items pour le mod Ex Nihilo
		- `#/exnihilocreatio/compressionRate` est le nombre de *pieces* pour avoir un *chunk* à cuire.
			N'est pris en compte que si `#/exnihilocreatio/addItems` est à *true*
		- `#/exnihilocreatio/modSieve/enabled` à *true* pour activer le craft dans le sieve
		- `#/exnihilocreatio/modSieve/<modid>:<item_id>:<metadata|-1>...` est le bloc à sieve (il peut y en avoir plusieurs)
		- `#/exnihilocreatio/modSieve/.*/drop` est l'item à drop, *count* le nombre, *chance* 0.0 -> 0% et 1.0 -> 100%,  
			*tier* est le *Mesh* et va de 1 à 4: 1 -> String, 2 -> Flint, 3 -> Iron, 4 -> Diamond
	- Extended Crafting:
		- `#/extendedcrafting/modSingularity/enabled` ajoute une singularité si est à *true*
		- `#/extendedcrafting/modSingularity/compression` est à défaut sur `ingot|12000`.  
			La première valeure est soit `none`, `ingot` ou `block`  
			La deuxième doit prendre `-1` si la première est `none`, ou pour utiliser la valeur par défaut qui est `12000`
- `<lingot_id>.png`
- `<lingot_id>_dust.png` si `#/hasDust` est à *true*
- `<lingot_id>_block.png` si `#/hasBlock` est à *true*
- `<lingot_id>_piece.png` si `#/exnihilocreatio/addItems` est à *true*
- `<lingot_id>_chunk.png` si `#/exnihilocreatio/addItems` est à *true*

### EXEMPLE

[Template](./ingot_template.json)

### ATTENTION

La taille du fichier compressé doit être strictement inférieure à 3.145.728 octets (3 Mo).
