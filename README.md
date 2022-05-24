В данной лабораторной работе я рассмотрю пример работы с утилиты ngrok с React-приложением.
===
Сначала нам потребуется установить node.js и npm.

``` 
sudo apt install nodejs 
sudo apt install npm 
```

Затем создaдим React-приложение при помощи команды:
 ``` npx create-react-app ngrok_test_app ```
 
 Переходим в созданный каталог и выполняем команду npm start
 ``` 
 cd ngrok_test_app 
 npm start 
 ```
 
 <img width="272" alt="image" src="https://user-images.githubusercontent.com/99497212/170045485-5bfa71a4-1985-4360-9655-2fdb1d2212c3.png">
 В результате мы создали данную веб-страницу
 
 <img width="579" alt="image" src="https://user-images.githubusercontent.com/99497212/170045670-f763cc3a-985b-423a-800d-b0629cb4c102.png">

Но если мы зайдем с другого устройства, подключенного к другой сети, то у нас ничего не покажет

![image](https://user-images.githubusercontent.com/99497212/170046079-820f7ff4-c864-4729-a45d-271e5ec78a15.png)

На помощь к нам прийдет ngrok, с его помощью мы сможем открыть порты и любой пользователь будет иметь доступ к сайту.
Запускаем программу ngrok и прописываем команду 
``` ngrok tcp 3000 ```
Где 3000 порт, которым мы пользуемся на предыдущем шаге.

<img width="434" alt="image" src="https://user-images.githubusercontent.com/99497212/170046712-5c06e789-42b7-46c7-9252-e84f4b9fff5e.png">

После этого, перейдя по ссылке 2.tcp.eu.ngrok.io:13728 на другом устройстве, откроется наш сайт.

![image](https://user-images.githubusercontent.com/99497212/170047099-d331ab0c-321e-40d1-b16b-9789e48eb6b4.png)
