<script type="text/javascript" src="https://maps.googleapis.com/maps/api/js"></script>
<script type="text/javascript" src="https://code.jquery.com/jquery-2.2.4.min.js"></script>
<input type="button" onclick="init_map()" value="cargar mapa" />
<?php 
	$cont = 2;
	$latitud  = array(20.6722467,20.6722561);
	$longitud = array(-103.2822466,-103.2826053);
	$precio   = array(2144,542);
	$tipop    = array(1,3);
	$usuario  = array("Pedro","Juan");
	$duracion = array("month","week");
?>
<div id="mapa"></div>
<script>
    var conta    = <?php echo $cont; ?>;
	var latitud  = new Array();
	var longitud = new Array();
	var usuario  = new Array();
	var precio   = new Array();
	var tipo     = new Array();
	var tiempo   = new Array();
	var latitud  = <?php echo json_encode($latitud);?>;
	var longitud = <?php echo json_encode($longitud);?>;
	var usuario  = <?php echo json_encode($usuario);?>;
	var precio   = <?php echo json_encode($precio);?>;
	var tipo     = <?php echo json_encode($tipop);?>;
	var tiempo   = <?php echo json_encode($duracion);?>;
function init_map() {
			var image = new google.maps.MarkerImage(
			'http://www.map.boun.edu.tr/css/img/lojman.png'
			);
            var myOptions = {
                zoom: 15,
                center: new google.maps.LatLng(latitud[0], longitud[0]),
                mapTypeId: google.maps.MapTypeId.ROADMAP
            };
            var map = new google.maps.Map(document.getElementById("mapa"), myOptions);
			for (i=0; i < conta; i++){
				var marker = new google.maps.Marker({
        	    	position: new google.maps.LatLng(latitud[i], longitud[i]),
                	map: map,
			    	icon: image,
					title: usuario[i] 
			        });
				var infowindow = new google.maps.InfoWindow({
                	content:'<a href="../info.php">precio[i]</a>' 
			    	});
			    	google.maps.event.addListener(marker, "click", function () {
                	infowindow.open(map, marker);
                	});	
			    	infowindow.open(map, marker);
			    	}
        }
		google.maps.event.addDomListener(window, 'load', init_map);
	           	
</script>
<style>
#mapa {width: 100%; height: 100%;}
</style>
