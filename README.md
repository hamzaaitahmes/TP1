                                 # HAMZA AIT AHMED G3 4IIRCIB #

                                         # TP1 {LAB1} #


                      Étape 1 — Télécharger Mobexler (OVA) et tracer le téléchargement

<img width="778" height="66" alt="image" src="https://github.com/user-attachments/assets/08467f7e-e2b2-4130-a93e-4d80ade709d2" />

Dans cette étape, la machine virtuelle Mobexler a été importée dans l’hyperviseur (VirtualBox ou VMware) à partir du fichier OVA fourni.
L’objectif est de disposer d’un environnement Android sécurisé et prêt pour les tests.
📌 Vérification : la VM apparaît dans la liste des machines et peut être sélectionnée pour démarrer.

                       Étape 2 — Importer l’OVA dans VirtualBox/VMware

<img width="818" height="860" alt="image" src="https://github.com/user-attachments/assets/66ecfec9-fee5-4a8c-a6cd-5ad06e99d320" />

La VM Mobexler a été démarrée avec succès.
Le bureau de Mobexler est accessible, ce qui confirme que le système fonctionne correctement après l’importation.
📌 Vérification : accès au bureau et aux menus Android, aucun message d’erreur au démarrage.

                            Étape 3 — Premier démarrage + connexion

<img width="1595" height="988" alt="image" src="https://github.com/user-attachments/assets/985832f2-16c2-438c-936f-7cb16c81e4ec" />

La connectivité réseau a été testée pour s’assurer que la VM peut accéder à Internet.

Le mode NAT a été configuré pour permettre l’accès externe

Les interfaces réseau et la route par défaut ont été vérifiées

Le ping vers une IP (8.8.8.8) et un nom de domaine (google.com) a été effectué
📌 Vérification : ping IP et ping DNS réussis, confirmant la connexion Internet.
 
                           Étape 4 — Vérifier le réseau (tests “santé”)

    Vérifier les interfaces réseau (IPs)
<img width="1276" height="843" alt="image" src="https://github.com/user-attachments/assets/698a3925-c1c1-4bcb-9190-04548ce92533" />


    Vérifier la route par défaut
<img width="1324" height="236" alt="image" src="https://github.com/user-attachments/assets/930a84f5-ec18-4d6f-9745-b0a3c9963cb0" />

    Tester la connexion Internet (IP)
<img width="1095" height="312" alt="image" src="https://github.com/user-attachments/assets/9ff10f53-054b-4458-a6c6-436de185e8d5" />

    Tester le DNS (nom de domaine)
<img width="1148" height="445" alt="image" src="https://github.com/user-attachments/assets/851e0087-1401-4515-8240-470e59385c93" />

Cette étape permet de vérifier l’état exact du réseau dans la VM :

Les interfaces réseau sont listées (ip a)

La route par défaut est vérifiée (ip route)

La connectivité Internet et DNS est testée (ping)
📌 Point de contrôle : Internet fonctionne via NAT, avec ping IP et ping DNS réussis.
Cela assure que la VM est prête pour les prochains tests réseau et ADB.

                              Étape 5 — Créer le snapshot “CLEAN” (baseline)

<img width="960" height="440" alt="image" src="https://github.com/user-attachments/assets/79d84a7e-3789-42b2-83f6-08f7feb7df63" />


Un snapshot nommé CLEAN_BASELINE_TP1 a été créé après validation du démarrage et de la connectivité réseau.

Objectif : conserver un point de restauration propre de la VM

Utilité : revenir à cet état avant chaque TP ou modification (installation de proxy, certificats, outils)
📌 Vérification : le snapshot apparaît dans VirtualBox/VMware et peut être restauré à tout moment.



                               Étape 6 — Préparer la cible Android (choisir 1 option)

                               
Cette étape permet de vérifier la connexion entre la VM Mobexler et un device Android, soit un smartphone réel via USB, soit un émulateur Android (Genymotion conseillé).

Option A — Smartphone USB :

Activation du mode développeur et USB Debugging sur le téléphone

Connexion du téléphone à la VM via USB

Vérification de la présence du device avec adb devices

Option B — Émulateur :

Démarrage d’un device Genymotion sur l’hôte

Connexion à ADB via l’IP du device (adb connect <IP_DEVICE>:5555)

Vérification que le device apparaît dans adb devices

📌 Point de contrôle :

Le device apparaît correctement dans ADB

La VM est prête pour les prochains tests Android

ADB fonctionne et peut communiquer avec le téléphone ou l’émulateur


                              
                            
