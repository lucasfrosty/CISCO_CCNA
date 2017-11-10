## Instruções

Primeiramente você vai precisar criar um servidor http local. Para isso usaremos o python, no seu terminal digite: 
```bash
python -m SimpleHTTPServer 8000
```

Agora basta você acessar o servidor que você acabou de criar, ele está localizado no http://localhost:8000

No meu caso funcionou apenas no Firefox, isso porque os outros browsers não estavam com o Flash Player instalados/habilitados. Para checar isso basta ir no console do Navegador (F12) e digitar o seguinte comando:

```js
let hasFlash = false;
try {
    hasFlash = Boolean(new ActiveXObject('ShockwaveFlash.ShockwaveFlash'));
} catch(exception) {
    hasFlash = ('undefined' != typeof navigator.mimeTypes['application/x-shockwave-flash']);
}
```

Se retornar ``false`` é porque o Flash não está instalado ou ativado, se retornar ``true`` é porque está.


## Habilitando o Flash no Chrome

### Parte1
No seu navegador, digite a url ``chrome://settings/content/flash`` (caso dê erro, significa que o você não tem o Flash Player instalado no seu navegador)
### Parte 2
Clique em ADD (caso seu Chrome seja em pt-BR o nome pode ser outro)
![alt text](https://github.com/lucasfrosty/CISCO_CCNA/blob/master/pt1.jpg "Logo Title Text 1")
### Parte 3
Agora basta colocar o endereço de http://localhost:8000 no espaço mostrado conforme a figura abaixo
![alt text](https://github.com/lucasfrosty/CISCO_CCNA/blob/master/pt2.jpg "Logo Title Text 1")  
 Pronto! Seu Google Chrome sempre irá habilitar o Flash para este site.
