# demo-springcloud-streams-kafka

# *****************************************************
# Zakaria EL Idrissi
# Master Intelligence Artificiel et Analyse De Données
# Faculté des sciences Meknès
# zak.elidrissi@edu.umi.ac.ma
# *****************************************************
 
<p>Dans cette partie, on va créer un broker Kafka.</p>

<h3>Le démarrage de kafka</h3>
<p>
 Alors pour démarrer kafka il faut de démarrer le serveur zookeeper, puis on va démarrer le serveur kafka
</p>

<p>Voici un exemple qui montre comment démarrer zookeeper et kafka</p>
<p>zookeeper utilise le port : 2181</p>
<p>kafka utilise le port : 9092</p>

![image](https://user-images.githubusercontent.com/61559275/172463937-71f61644-e9a4-43e7-9326-bbbc2e373223.png)

![image](https://user-images.githubusercontent.com/61559275/172465006-9494cfaa-9ac5-4f46-81c7-cf5eed5a3758.png)

<h3>La phase de test</h3>

<p>
 Pour faire un test, il faut de démarrer le consommer pour consommer les messages envoyés par le producer.
 puis il faut de démarrer le producer prour envoyé des messages à le consumer.
</p>

<p>Voici un exemple : </p>

<h4>Consumer : </h4>

![image](https://user-images.githubusercontent.com/61559275/172466733-ed68ac2f-5e1b-440a-ab12-7f58ee7721bb.png)

<h4>Producer : </h4>

![image](https://user-images.githubusercontent.com/61559275/172467134-e068a414-f8c6-4f4e-8817-ed74b1a3e269.png)

<p>quand les deux est démarrer, On va envoyé un message du producer au consumer</p>
<p>Voici un exemple : </p>

![image](https://user-images.githubusercontent.com/61559275/172467883-7e3ea3c7-578a-46f8-a847-e7e2ca243a2d.png)

<p>
 Maintenant on va créer une application spring boot, On va commence par créer d'abord notre contrôleur.<br>
 D'abord on va créer notre entitie qu'on appelle "PageEvent", puis on va créer notre rest controller qu'on appelle "PageEventRestController".<br>
 on va créer dans notre contrôleur on fonction qui peut de publier un PageEvent sur un topic.
</p>

<p>
 Voici un exemple :
</p>
 
![image](https://user-images.githubusercontent.com/61559275/172484113-94faa6dd-b349-45db-b291-c056fcf89769.png)

<p>
 Puis on va créer un service qu'on appelle "PageEventService" qui contient une fonction de type Consumer qui reçoi une input et retourne une un objet de type  PageEvent.
</p>

<p>Voici un exemple : </p>

![image](https://user-images.githubusercontent.com/61559275/172487020-c4e879ca-1cd8-4785-9f5e-8572ef60bd6a.png)

![image](https://user-images.githubusercontent.com/61559275/172487067-f6a19016-4af1-4e93-a846-4428e11e106c.png)

<p>
 Puis on va créer un autre fonction de type Supplier qui produire des objets de type PageEvent et qui retourne dans chaque second un objet de type PageEvent.<br>
</p>

![image](https://user-images.githubusercontent.com/61559275/173156524-b0303c39-98bd-4fdd-87d8-b959dbaccd78.png)

<p>
 puis on va créer une fonction de type Function qui fait à la fois le role de producer et consumer<br>
 Voici un exemple
</p>

![image](https://user-images.githubusercontent.com/61559275/173158203-4fe67838-9752-4f92-8696-c9d5f0b8bef0.png)

<p>
 Après pour traiter les flux de message en temps réel nous avons utilisés kafka stream :
</p>

![image](https://user-images.githubusercontent.com/61559275/173159182-41fa3bbf-86f0-497f-b694-0406ce160340.png)


![image](https://user-images.githubusercontent.com/61559275/173159147-8814c43d-e247-4490-a304-3ab411f26ee1.png)

<p>
 Pour utiliser les résultats provenant de ktable dans une application on peut les percister dans un store :<br>
 Interroger Kafka-streams Store avec Server Sent Event : <br>
 Une fois le client établit une connexion http (la connexion reste ouverte), le serveur va poucer les données vers le client
</p>

![image](https://user-images.githubusercontent.com/61559275/173188873-3d52e63c-5263-4708-a311-f92ea90b8b1f.png)


<p>Client HTML Server Sent Event :</p>

![image](https://user-images.githubusercontent.com/61559275/173160249-1f4fc1a5-e4df-4b25-b059-0c06a6cd8fcc.png)





