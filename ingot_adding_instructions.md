AJOUT D'UN LINGOT POUR LE MODPACK "Infinite Cadriz":
====================================================

Si tu veux proposer des lingots � rajouter au modpack "Infinite Cadriz", envoie ton zip "<lingot_id>.zip" qui est le compress�
du dossier "<lingot_id>" avec:

FICHIER TEXTE:
--------------

- "<lingot_id>.json" sur la base de "lingot_template.json":
	- ".crafting.smelting" est � mettre sur "-1.0" si:
		1) ".hasDust" est false
		2) ou pour d�sactiver le four.
		Cela correspond � l'xp gagn�.
	- ".crafting.compress" et ".crafting.uncompress" doivent �tre � {"type": "none"} pour enveler le craft.
		Sinon mettre "crafting_shaped" ou "crafting_shapeless".
	- ".exnihilocreatio.modSieve.enabled" � "true" pour activer le craft dans le sieve
	- ".exnihilocreatio.modSieve.<modid>:<item_id>:<metadata|-1>..." est le bloc � sieve
	- ".exnihilocreatio.compressionRate" est le nombre de "piece" pour avoir un "chunk" � cuire.
		N'est pris en compte que si ".exnihilocreatio.addItems" est � true
	- ".exnihilocreatio.modSieve.*.drop" est l'item � drop, "count" le nombre, "chance" 0.0 -> 0% et 1.0 -> 100%, "tier" va de 1 � 4:
		1 -> String, 2 -> Flint, 3 -> Iron, 4 -> Diamond Mesh
	- ".extendedcrafting.modSingularity.enabled" ajoute une singularit� si est � "true"
	- ".extendedcrafting.modSingularity.compression" est � d�faut sur "ingot|12000". La premi�re valeure est soit "none", "ingot" ou "block"
		La deuxi�me doit prendre "-1" si la premi�re est "none", autrement le d�faut est de "12000"

FICHIER.S IMAGE.S (1 � 5):
--------------------------

- "<lingot_id>.png"
- "<lingot_id>_dust.png" si ".hasDust" est � true
- "<lingot_id>_block.png" si ".hasBlock" est � true
- "<lingot_id>_piece.png" si ".exnihilocreatio.addItems" est � true
- "<lingot_id>_chunk.png" si ".exnihilocreatio.addItems" est � true

### ATTENTION

La taille du ".zip" doit �tre inf�rieur strict � 3.145.728 octets (3 Mo).