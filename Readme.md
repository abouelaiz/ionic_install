# Guide d'installation ionic project
##  Qu’est-ce que Ionic Framework ?

 Ionic Framework est un mélange d’outils et de technos pour développer des applications mobiles hybrides rapidement et facilement. Il s’appuie sur AngularJS pour la partie application web du framework et sur Cordova  pour la partie construction des applications natives. 
##  Comment on procéde créer un projet ionic ? 
1. Pour générer une application mobile hybride, il vous faut le SDK Java et le SDK Android c'est pourquoi je vous invite à:

     Télécharger et installer Java SE developpement Kit    [lien de téléchargement](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) 
     
    Télécharger et installer android sdk   [lien de téléchargement](http://developer.android.com/sdk/index.html#Othe), 
    il faut juste ne pas oublier d'ajouter les variables d’environnement de système.
    
    Pour windows :
    ```cmd
     set ANDROID_HOME=C:\Users\<user_name>\Library\Android\sdk
     set PATH=%PATH%;%ANDROID_HOME%\tools;%ANDROID_HOME%\platform-tools
    ```
     Pour Mac :
    ```cmd
     export ANDROID_HOME=/<installation location>/android-sdk-macosx
     export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
    ```
    
    
2. Ensuite la deuxiéme chose a faire c'est de télécharger et installer Nodejs pour la simple raison c'est que ionic a besoin de npm pour  installer et gérer les dépendances entre les modules dont il a besoin  . 
    [lien de téléchargement](https://nodejs.org/en/)
3. installer ionic et cordova 
    ```cmd
     npm install -g cordova ionic
    ```
4. créer votre projet ionic 

    ```javascript
    //blank pour un projet vide 
     ionic start Garagiste blank
    ```
   ![alt text](https://github.com/abouelaiz/ionic_install/blob/master/images/start.PNG " Logo Title Text 1")
   
   la structure de notre projet 
   
      ![alt text](https://github.com/abouelaiz/ionic_install/blob/master/images/structure.PNG " Logo Title Text 1")
    * Platforms : ce répértoire contiendra le build de nos projet ios et android (APK et XcodeProject).
    * Plugins   : c'est dans ce repertoire que cordova stocke les plugins que nous ajoutons à notre projet.
    * SCSS      : c'est ici où nous allons stocké nos fichiers .Scss.
    * WWW :      en gros c'est notre fameux répértoire app c'est le répertoire où nous ecrivons tous fichiers sources  JS/HTML/CSS ....
    * RESSOURCES: c'est dans ce répértoire où on stocke  tous les resoources nécessaire pour le build comme les icones,  les splashscreens ...
5. Pour simuler notre application dans le navigateur 

   ```cmd
    ionic serve
    ```
    une autre commande utilisé pour simulé dans le navigateur et qui nous donne une idée à quoi ressemblerai notre app sur Android et IOS
   ```cmd
    ionic serve --lab
    ```
    
    ![alt text](https://github.com/abouelaiz/ionic_install/blob/master/images/lab.PNG "Logo Title Text 1")
     
     sinon pour ajouter un plugin a notre projet 
      ```cmd
    ionic plugin add {plugin}
    ```
     
6. Enfin on est arrivé  au  build   de l'application  

   on commence par ajouter notre platforme cible

    ```cmd
    // pour android
    ionic platform add android
    // pour IOS
    ionic platform add ios
    ```
    esuite on build notre application pour la platform cible

    ```cmd
    // pour android (on récupére un Apk non signé)
     ionic build anroid 
    // pour IOS (on récupére un xcodeproject)
     ionic build IOS
    ```    
    
