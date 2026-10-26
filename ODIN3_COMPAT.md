# Compatibilité Odin 3 : ARMSX2 (PS2)

Notre propre liste de compatibilité, tenue d'après nos tests sur l'AYN Odin 3 (Snapdragon 8 Elite, Adreno 830) avec notre build de la branche `odin3`. Chaque test met à jour la ligne du jeu : statut, mesure, date et commit testé. Amont : https://github.com/ARMSX2/ARMSX2

## Échelle

| Statut | Sens |
|---|---|
| 🟢 Parfait | vu en partie, plein régime, aucun défaut vu |
| 🔵 Jouable | vu en partie, défauts mineurs |
| 🟡 Problèmes | vu en partie, défauts gênants (fps, graphismes, son) |
| 🟠 Menus/intro | démarre, pas encore vu en partie |
| 🔴 Ne marche pas | crash, écran noir ou blocage |
| ⚪ Non testé | présent sur la console, jamais lancé |

## Comment on teste

Labo commun `odin3-lab` (VM ARM64 pages 4 Ko + profil Vulkan de l'Adreno 830) pour le CPU et la logique, puis l'Odin 3 par adb pour le GPU, les fps et la chauffe.

## Jeux

| Jeu | Statut | Vu jusqu'à | Mesure | Notes | Testé le | Build |
|---|---|---|---|---|---|---|
| Dragon Ball Z: Budokai Tenkaichi 3 (PAL, SLES-54945) | 🟢 | combat Raditz (Dragon History, Saga Saiyan), 1 min | 6x (~4K) : 50 fps (100 %), GPU 79-86 %, EE 31-34 % ; 1x : 50 fps, GPU ≤ 18 % | Vulkan (Auto), patchs GameDB ; son non vérifié ; manettes façon Switch (7568b0f8a, vu le 26/10 docké, lancé par ES-DE) : un appui fait rejoindre une manette en J1 si l'Odin le tient, sinon en J2 (DS4 en J1, manette suivante en J2 qui choisit son perso en « J1 VS J2 »), l'Odin reprend J1 dès que les autres sont libres ; le port 2 n'est branché qu'au lancement s'il y a 2 manettes ou plus | 2026-10-26 | odin3 7568b0f8a |
