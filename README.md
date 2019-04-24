# ChienChat512
SSD Mobilenet 512

fichiers:
´´´gen_model.sh´´´ permet de créer les fichier prototxt (train, test et deploy dans le repertoire example)
´´´create_lmdb.sh´´´ permet de créer les fichier db pour le train.
´´´train.sh´´´ trainer , crée des fichier iteration dans le repertoire snaphot.
´´´demo.py´´´ fichier de test _iter_xxx.caffemodel sur des images. 
´´´test.py´´´ fichier test _iter_xxx.caffemodel sur la webcam.
Progression dans le Mobilenet SSD.
L'augmentation de la definition 300*300 à 512*512 permet d'être plus précis dans la détection.
La compilation en graph ne peut se faire avec le raspberry pi (memory Error).
On compile le fichier deploy et caffemodel en fichier graph et on l'envoie vers le rapsberry.


Si on utilise une definition de camera 640*480,
SSD Mobilenet 640*480 evite un resize dans le process d'empilement dans le sitck movidius.
On rechange les fichiers prototxt (deploy, train et test) en 640*480.
->gen_model.sh
->create_lmdb.sh
->train.sh pour avoir minimum 50000 iteration.
ne pas oublier de modifier les fichier test.py et demo.py pour les essais sur pc.
