# Emoji-Jquery-PHP-Mysql-
<h3>Exemplo e explicação de como inserir emoji no banco de dados com Jquery (Ajax) e php.</h3> 
<p>Para fazermos a inserção de emoji no banco de dados, seje ele MySql ou outros tipos, não necessariamente precisamos de uma tebela ou um banco de dados com utf8mb4, pois o que queremos armazenar são apenas caracteres, mas uma grande pergunta vem, como faz isso menino?</p>
<p>Para fazermos isso, iremos utilizar a biblioteca do <em><b>emojione</b></em> <a href="https://demos.emojione.com/latest/index.html#extras">Acessar emojione</a>Essa biblioteca tem funções JavaScript que codificam e decodificam um emoji, isto é, para armazenar ele no banco, iremos codificar, e depois decodificar para serem enterpretados em dispostivos (IOS, Android e para Web)</p>
<p>Então vamos ao que interessa</p>
```
<script src="https://cdn.jsdelivr.net/npm/emojione@4.0.0/lib/js/emojione.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/emojione@4.0.0/extras/css/emojione.min.css"/>
```
