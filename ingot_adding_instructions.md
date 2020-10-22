AJOUT D'UN LINGOT POUR LE MODPACK "Infinite Cadriz":
====================================================

Si tu veux proposer des lingots à rajouter au modpack "Infinite Cadriz", envoie ton zip "<lingot_id>.zip" qui est le compressé
du dossier "<lingot_id>" avec:

FICHIER TEXTE:
--------------

- "<lingot_id>.json" sur la base de "lingot_template.json":
	- ".crafting.smelting" est à mettre sur "-1.0" si:
		1) ".hasDust" est false
		2) ou pour désactiver le four.
		Cela correspond à l'xp gagné.
	- ".crafting.compress" et ".crafting.uncompress" doivent être à {"type": "none"} pour enveler le craft.
		Sinon mettre "crafting_shaped" ou "crafting_shapeless".
	- ".exnihilocreatio.modSieve.enabled" à "true" pour activer le craft dans le sieve
	- ".exnihilocreatio.modSieve.<modid>:<item_id>:<metadata|-1>..." est le bloc à sieve
	- ".exnihilocreatio.compressionRate" est le nombre de "piece" pour avoir un "chunk" à cuire.
		N'est pris en compte que si ".exnihilocreatio.addItems" est à true
	- ".exnihilocreatio.modSieve.*.drop" est l'item à drop, "count" le nombre, "chance" 0.0 -> 0% et 1.0 -> 100%, "tier" va de 1 à 4:
		1 -> String, 2 -> Flint, 3 -> Iron, 4 -> Diamond Mesh
	- ".extendedcrafting.modSingularity.enabled" ajoute une singularité si est à "true"
	- ".extendedcrafting.modSingularity.compression" est à défaut sur "ingot|12000". La première valeure est soit "none", "ingot" ou "block"
		La deuxième doit prendre "-1" si la première est "none", autrement le défaut est de "12000"

FICHIER.S IMAGE.S (1 à 5):
--------------------------

- "<lingot_id>.png"
- "<lingot_id>_dust.png" si ".hasDust" est à true
- "<lingot_id>_block.png" si ".hasBlock" est à true
- "<lingot_id>_piece.png" si ".exnihilocreatio.addItems" est à true
- "<lingot_id>_chunk.png" si ".exnihilocreatio.addItems" est à true

### ATTENTION

La taille du ".zip" doit être inférieur strict à 3.145.728 octets (3 Mo).