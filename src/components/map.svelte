<script>
	import L from 'leaflet';
	import 'leaflet/dist/leaflet.css';

	let mapState = {
		id: 'map',
		latitude: 30.149,
		longitude: -95.5379,
		zoom: 18
	};

	$effect(() => {
		let map = L.map(mapState.id);
		L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
			maxZoom: 19,
			attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
		}).addTo(map);
		map.setView([mapState.latitude, mapState.longitude], mapState.zoom);

		var polygon = L.polygon([
			[51.509, -0.08],
			[51.503, -0.06],
			[51.51, -0.047]
		]).addTo(map);
	});
</script>

<div id="map"></div>

<style>
	@import url('https://unpkg.com/leaflet@1.9.4/dist/leaflet.css');
	#map {
		height: 640px;
	}
</style>
