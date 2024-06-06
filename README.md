# Mapas
Caixa de Mapa

Adicionando dependências e configurações no projeto:  Adicione a dependência do MapBox ao seu arquivo “build.gradle” :
implementação 'com.mapbox.mapboxsdk:mapbox-android-sdk:10.3.1'

No arquivo “AndroidManifest.xml”, adicione as permissões para acesso ao GPS:

Obtendo a localização pelo GPS: Para acessar a localização pelo GPS, você pode usar a classe “LocationManager” ou as APIs de localização do Google Play Services.
Simulando a localização no emulador: No Android Studio, você pode simular a localização do dispositivo usando o "Simulador de Localização" na barra de ferramentas.
Adicionando uma marcação no mapa:
// Obtendo uma referência do mapa val mapView = findViewById(R.id.mapView) mapView.getMapAsync { mapboxMap -> // Adicionando marcador na localização atual val markerOptions = MarkerOptions() .position(LatLng(latitude, longitude)) .title ("Minha Localização") mapboxMap.addMarker(markerOptions) }

API do Google Maps

Adicionando dependências e configurações no projeto:  Adicione a dependência da API do Google Maps no seu arquivo “build.gradle”:
implementação 'com.google.android.gms:play-services-maps:18.0.0'

No arquivo “AndroidManifest.xml”, adicione a chave da API e as permissões de localização:

Obtendo a localização pelo GPS: Você pode usar as classes “FusedLocationProviderClient” ou “LocationManager” para obter a localização atual do dispositivo.
Simulando a localização no emulador: Acesse as configurações do emulador, vá para "Dispositivo Emulado" e insira as coordenadas de latitude e longitude para simular a localização.
Adicionando uma marcação no mapa:
// Obtendo uma referência do mapa val mapFragment = supportFragmentManager.findFragmentById(R.id.map) as SupportMapFragment mapFragment.getMapAsync { googleMap -> // Adicionando marcador na localização atual val markerOptions = MarkerOptions() .position(LatLng(latitude, longitude )) title("Minha Localização") googleMap.addMarker(markerOptions) }
