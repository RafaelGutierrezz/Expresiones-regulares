<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="es" lang="es">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
<title>Validación con expresión regular</title>
<script type="text/javascript">
function literal() {


  var n = document.getElementById("nombre").value;
  var expreg = /^([a-zA-Z]{1,20})$/;

  if(expreg.test(n))
	alert("El nombre es correcto");
  else
    alert("El nombre debe contener solo letras");


    var c = document.getElementById("correo").value;
    var expreg = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,4})+$/;

    if(expreg.test(c))
  	alert("El correo es correcto");
    else
      alert("El correo es icorrecto... EJ:xxx-000@xxxxx.xxx");

      var t = document.getElementById("telefono").value;
      var expreg = /^([0-9]{1,10})+$/;

      if(expreg.test(t))
    	alert("El telefono es correcto");
      else
        alert("El telefono es incorrecto");

      var m = document.getElementById("matricula").value;
      var expreg = /^([a-zA-Z]{3}-\d{3})$/;

      if(expreg.test(m))
    	alert("La placa es correcta");
      else
        alert("La placa no es correcta. EJ: AAA-000");
}

function objeto() {

  var n = document.getElementById("nombre").value;
var expreg = new RegExp("^([a-zA-Z]{1,20})$");

  if(expreg.test(n))
    alert("El nombre es correcto");
    else
      alert("El nombre debe contener solo letras");


    var c = document.getElementById("correo").value;
  var expreg = new RegExp("^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,4})+$");

    if(expreg.test(c))
      alert("El correo es correcto");
    else
      alert("La correo es incorrecto");


      var t = document.getElementById("telefono").value;
    var expreg = new RegExp("^([a-zA-Z]{3}\-\d{3})$");

      if(expreg.test(t))
        alert("El teledono es correcto");
      else
        alert("El telefono es icorrecto");


          var m = document.getElementById("matricula").value;
        var expreg = new RegExp("^([a-zA-Z]{3}\-\d{3})$");

          if(expreg.test(m))
            alert("La matrícula es correcta");
          else
            alert("La matrícula NO es correcta");


}
</script>
</head>
<body>
<form id="miForm" action="" method="get">
<p>
  Nombre: <input type="text" id="nombre" />
  <br /> Correo: <input type="text" id="correo" />
  <br /> Telefono: <input type="text" id="telefono" />
  <br /> Placas: <input type="text" id="matricula" />

<br />
<br />

<input type="button" value="Validar Literal" onclick="literal()" />
<input type="button" value="Validar Objeto" onclick="objeto()" />
</p>
</form>
</body>
</html>
