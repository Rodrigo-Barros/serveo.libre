# SERVEO LIBRE
Este projeto visa detectar uma possivel falha na conexão do serveo e quando acontecer reiniciar a conexão e notificar o usuario através do telegram com o novo link gerado.

## Antes de iniciar
renomeie o arquivo .env.sample para .env, para conseguir.

## Exemplos de uso
1. `./serveo.libre` Dessa forma vamos redirecionar o tráfego do serveo.net da porta 80 para nossa porta 8080 local.
2. `./serveo.libre -p 80:9000`, dessa forma podemos redirecionado o tráfego originado da porta 80 do servidor serveo.net para a nossa porta local 9000, podendo assim desmontrar nossa aplicação para o mundo.
3. `./serveo.libre -p 2000:22` similar aos demais comandos porém nessa caso estamos redirecionado um trafego tcp do porta 2000 do serveo.net para nosso servidor ssh na nossa porta local 22.
4. `serveo.libre -R incubo:80:localhost:9000` dessa forma podemos fornecer argumentos diretamento para o comando ssh.

# Configurando o envio de mensagens com o telegram
Não vou entrar em muitos detalhes de como obter as chaves da API e o CHAT_ID.

1. renomeie o arquivo .env.sample para .env
2. Altere os valores das variaveis API_TOKEN e CHAT_ID, para os valores obtidos no telegram. Após isso salve e inicie o serviço para ver se tudo funciona como deveria.

# Depurando
Existem duas variaveis que podem ser utilizadas para encontrar enventuas problemas na conexão são elas:
    
    - DEBUG=1 Aumenta a verbosidade do script mostrando o que está ocorrendo
    - LOG=nomearquivo Cria um arquivo na pasta aonde o script está sendo excutando para ajudar a encontrar enventuais falhas.