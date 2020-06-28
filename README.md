# SiteTune Docker MultipleStream #

## Sobre/About ##

### Português do Brasil ###
Com esse projeto você poderá fazer transmissões simultâneas para YouTube e Facebook.
Para o YouTube usamos o método tradicional com protocolo RTMP.
Para o Facebook usamos o stunnel para possibilitar a transmissão para o protocolo RTMPS do Facebook.
Você pode adicionar outros serviços de stream como a Twitch.tv de maneira semelhante à do YouTube.
Esse projeto trata-se de uma imagem docker pré-configurada com stunnel, nginx e o plugin nginx-rtmp. 
Você só precisa compilar a imagem e configurar o arquivo nginx.conf com suas chaves de transmissão como no exemplo abaixo.

Onde estiver XXXX-XXXX-XXXX-XXXX você coloca sua chave do YouTube.

Onde estiver XXXXXXXXXXXXXXXX?ds=1&s_l=1&a=XXXXXXXXXXXXXXXX você coloca sua chave do Facebook.

### English ###
With this project you will be able to broadcast simultaneously to YouTube and Facebook.
For YouTube we use the traditional method with RTMP protocol.
For Facebook we use the stunnel to enable transmission to the Facebook RTMPS protocol.
You can add other streaming services like Twitch.tv in a similar way to YouTube.
This project is a docker image pre-configured with stunnel, nginx and the nginx-rtmp plugin.
You just need to compile the image and configure the nginx.conf file with your transmission keys as in the example below.

Where you have XXXX-XXXX-XXXX-XXXX put your YouTube key.

Where you have XXXXXXXXXXXXXXXX?ds=1&s_l=1&a=XXXXXXXXXXXXXXXX put your Facebook key.

###Exemplo/Example###
```
push rtmp://a.rtmp.youtube.com/live2/XXXX-XXXX-XXXX-XXXX;
push rtmp://127.0.0.1:1936/rtmp/XXXXXXXXXXXXXXXX?ds=1&s_l=1&a=XXXXXXXXXXXXXXXX;
```