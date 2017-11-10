## Instructions

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

1. No seu navegador, digite a url ``chrome://settings/content/flash`` (caso dê erro, significa que o você não tem o Flash Player instalado no seu navegador)
2. Em seguida, procure a seguinte opção: 
![alt text](https://github.com/lucasfrosty/CISCO_CCNA/pt1.jpg"Parte 1")  
Ao clicar em ADD (caso seu Chrome seja em pt-BR o nome pode ser outro), será aberta uma caixa conforme mostra a imagem abaixo
3. ![alt text](https://github.com/lucasfrosty/CISCO_CCNA/pt2.jpg"Parte 2")  
Basta colocar o endereço de http://localhost:8000 no espaço mostrado na figura e pronto! Seu Google Chrome sempre irá habilitar o Flash (ps: apenas para esse site).
