# Cyberpunk-Optimisation

  - [Introduction](#introduction)
  - [Installation de ce repot](#installation-de-ce-repot)
  - [Cyberpunk Paramètre](#cyberpunk-paramètre)
  - [Pool de mémoire (memory_pool_budgets.csv)](#pool-de-mémoire-memory_pool_budgetscsv)
  - [CPU AMD et Intel](#cpu-amd-et-intel)
  - [GPU Nvidia](#gpu-nvidia)
  - [Clavier AZERTY](#clavier-azerty)
  - [Reshader](#reshader)

## Introduction
Cyberpunk est un beau jeu et, contrairement aux idées reçues, il est assez bien optimisé. Mais la sortie de Cyberpunk a été clairement précipitée et il y a des problèmes flagrants qui doivent être résolus.

## Installation de ce repot
1. Allez dans le dossier de votre jeux Ex. "C:\Program Files (x86)\GOG Galaxy\Games\Cyberpunk 2077\bin\x64".
2. Coller tout les fichier Téléchargé dans ce dossier.
3. Ajuster les paramètres [CPU AMD et Intel](#cpu-amd-et-intel)

## Cyberpunk Paramètre
Tout d'abord, je vais commencer par les paramètres généraux et leurs publics cibles.
- Les réglages bas sont évidemment destinés aux systèmes à faible consommation d'énergie.
- Les réglages moyens sont en fait destinés au standard moderne des systèmes de milieu de gamme. Utilisez des paramètres moyens si vous jouez à 1080p, en particulier une résolution de texture. Si vous jouez à 1080p et que vous utilisez les paramètres de texture élevés, vous filmez votre FPS dans le pied pour à peine des gains visuels.
- Les réglages High et Ultra sont destinés à la 4K. Comme dans, vous auriez besoin d'un moniteur 4K pour voir même ce que font même les paramètres élevés ou ultra. Les seules exceptions à cela sont la qualité de l'ombre, le niveau de détail, les effets de prétraitement et de post-traitement (précision des couleurs, anticrénelage, RTX, DLSS, SSAO, SSS, Volumetrics).

## Pool de mémoire (memory_pool_budgets.csv)
Parlons de l'erreur la plus flagrante de CD Projekt Red: le fichier de budget de pool de mémoire. Pour faire simple, CDPR a poussé le mauvais fichier sur le PC.

Par défaut, l'application n'aura accès qu'à un maximum de 1,5 Go de RAM et 3 Go de VRAM, ce qui est bien inférieur à ce que le joueur PC moyen a sous la main. 

C'est ce qui cause des fréquences d'images extrêmement faibles sur des systèmes relativement puissants.

## CPU AMD et Intel
Enfin, nous parlerons d'autres modifications que vous pouvez utiliser pour améliorer les performances et la stabilité. Vous pouvez utiliser le patch de [yamashi](https://github.com/yamashi/PerformanceOverhaulCyberpunk/wiki). Vous pouvez configurer le AVX : "dans performance_overhaul/config.json"

Si vous ne savez pas si vous devez utiliser un correctif AVX, [CPU-Z](https://www.cpuid.com/softwares/cpu-z.html) peut vous montrer une liste de jeux d'instructions pris en charge par votre CPU. N'utilisez pas de correctif AVX si votre CPU le prend en charge, cela pourrait nuire aux performances.

## GPU Nvidia
Chers utilisateurs de GPU NVIDIA: veuillez ouvrir le panneau de configuration NVIDIA et forcer «Haute performance» sur «Filtrage de texture - Qualité» sous Paramètres 3D du gestionnaire. Il y a peu ou pas de différence perceptible entre haute performance et haute qualité, et cela vous rapportera 2 ou 3 FPS supplémentaires.

## Clavier AZERTY
Ce mod modifie le fichier "inputUserMappings.xml"
- Il change toutes les entrées QWERTY en entrée par défaut AZERTY.
- MAP est sur la touche virgule. (Vous pouvez le modifier, recherchez "IK_Comma" bind).

## Reshader
1. Installez la dernière version de [ReShade](https://reshade.me/)
2. Installez le Reshader dans votre dossier bin\x64. Ex. "C:\Program Files (x86)\GOG Galaxy\Games\Cyberpunk 2077\bin\x64".
Vous pouvez être invité à écraser les fichiers si vous avez déjà installé des packages shader lorsque vous avez installé ReShade. 
3. Démarrez le jeu et appuyez sur Début. Sélectionnez AA Blender.ini dans la liste déroulante en haut.
