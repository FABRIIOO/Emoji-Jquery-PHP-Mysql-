# Emoji-Jquery-PHP-Mysql-
<h3>Exemplo e explicação de como inserir emoji no banco de dados com Jquery (Ajax) e php.</h3> 
<p>Para fazermos a inserção de emoji no banco de dados, seje ele MySql ou outros tipos, não necessariamente precisamos de uma tebela ou um banco de dados com utf8mb4, pois o que queremos armazenar são apenas caracteres, mas uma grande pergunta vem, como faz isso menino?</p>
<p>Para fazermos isso, iremos utilizar a biblioteca do <em><b>emojione</b></em> <a href="https://demos.emojione.com/latest/index.html#extras">Acessar emojione</a>Essa biblioteca tem funções JavaScript que codificam e decodificam um emoji, isto é, para armazenar ele no banco, iremos codificar, e depois decodificar para serem enterpretados em dispostivos (IOS, Android e para Web)</p>
<p>Então vamos ao que interessa. Faça o Download ou simplesmente cole estes links no seu no cabeçalho da sua pagina.</p>

```
<script src="https://cdn.jsdelivr.net/npm/emojione@4.0.0/lib/js/emojione.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/emojione@4.0.0/extras/css/emojione.min.css"/>

```
<p>Feito isso vamos fazer nossa codificação</p>
<pre>
  var msg = "oii! 🐶";
  msg = emojione.toShort(msg);
</pre>
<p>Este dado codificado armazenado na variavel (msg) pode ser passado sem problema nenhum, para um Ajax ou Axios entre outros tipos.</p>
<pre>

     $.ajax({
         url :"Arquivo php ",
         type : 'post',
            data : {
              "F": "EnviandoMsg",
               "msg": msg
            },
          }).done (function(retorno){
               var msg = emojione.shortnameToUnicode(retorno); //msg decodificada 
              alert(msg);
       });
</pre>
<p>Perceba que decodificamos no retorno do Ajax </p>
