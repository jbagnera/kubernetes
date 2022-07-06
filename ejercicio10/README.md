
-Para probarlo directamente con docker:

    docker run -d -e TELEGRAM_TOKEN=token nicopaez/telegrambot:0.0.7

    pruebo conversación

-para para desplegar el bot en minikube:
   use como base otro descriptor:
     wget https://gitlab.com/-/snippets/2088421/raw/master/deployment.yaml
   lo adapte para correr el bot de telegrambot:
     env:
       - name: TELEGRAM_TOKEN
         value: "token"
   desplego con kubernetes:
      kubectl apply -f deployment.yaml
   pruebo conversación 
