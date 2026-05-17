# tp-18


<img width="328" height="581" alt="1" src="https://github.com/user-attachments/assets/f30bc90c-e3cd-45cd-82f5-e7a7ba7c9c81" />
<img width="1658" height="871" alt="2" src="https://github.com/user-attachments/assets/1c9c113b-2246-4757-9103-fb59887b8451" />

Analyse du contenu
Fichier 1.png (interface utilisateur)
Valeur affichée : 3

Trois boutons :

INCRÉMENTER

DÉCRÉMENTER

RÉINITIALISER

Fichier 2.png (code source / logs Android Studio)
Projet Android : com.example.viewmodellivedatademoei / com.example.viewmodellivedatademoenrichi

Architecture utilisée : ViewModel + LiveData (architecture recommandée par Google)

Composants identifiés :

CounterViewModel (5 usages)

MainActivity (12 usages)

tvCount (TextView pour afficher la valeur)

btnIncrement, btnDecrement, btnReset (boutons)

Code observé :

java
viewModel = new ViewModelProvider(this).get(CounterViewModel.class);
tvCount = findViewById(R.id.tvCount);
btnIncrement = findViewById(R.id.btnIncrement);
btnDecrement = findViewById(R.id.btnDecrement);
btnReset = findViewById(R.id.btnReset);
Log de succès : "Install successfully finished in 164 ms" et "App restart successful without requiring a re-install"

Conclusion
 L’application Android fonctionne correctement et implémente un compteur (valeur = 3) avec les fonctionnalités suivantes :

Action	Effet attendu
INCRÉMENTER	Augmente la valeur affichée (3 → 4 → 5 ...)
DÉCRÉMENTER	Diminue la valeur affichée (3 → 2 → 1 ...)
RÉINITIALISER	Remet la valeur à 0 (ou une valeur par défaut)
Points techniques validés :
ViewModel : survit aux changements de configuration (rotation écran, etc.)

LiveData (probable) : mise à jour automatique de l’interface

Installation et exécution : succès en 164 ms

Redémarrage de l’app : réussi sans réinstallation
