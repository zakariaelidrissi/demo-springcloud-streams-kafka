# demo-springcloud-streams-kafka
 
<p>Dans cette partie, on va créer un broker Kafka.</p>

<h3>Le démarrage de kafka</h3>
<p>
 Alors pour démarrer kafka il faut de démarrer zookeeper, puis on va démarrer kafka
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





