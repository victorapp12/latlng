latlng
======

Distância entre dois pontos lat lng 

//Victor Palhares
//victorpalhares.com

public function Calcula_Distancia($latitude1, $longitude1, $latitude2, $longitude2){	
		
		$rad_lat = $latitude1 * 0.0174532925;
		$rad_lng = $longitude1 * 0.0174532925;
		$rad_lat2 = $latitude2 * 0.0174532925;
		$rad_lng2 = $longitude2 * 0.0174532925;
		
		$cosS = sin($rad_lat2)*sin($rad_lat)+cos($rad_lat2)*cos($rad_lat)*cos($rad_lng2-$rad_lng);
		
		$S1 = acos($cosS);

		$S2 = 180*($S1);

    $raioTerra = 6378;
		$distancia = $raioTerra * $S1;
		
		echo 'distancia(km): '.$distancia;
		
		}