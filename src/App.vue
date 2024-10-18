<template>
	<div class="d-flex flex-column vh-100">
		<header class="navbar navbar-expand navbar-dark bg-dark shadow flex-shrink-0">
			<div class="container-fluid">
				<div class="navbar-brand my-1">
					<i class="bi bi-router-fill text-secondary h2 align-middle me-3"></i>
					<a class="text-light align-middle d-sm-inline d-none" href="https://github.com/italofds" target="_blank">italofds</a>
					<span class="text-secondary align-middle d-sm-inline d-none"> / </span>
					<a class="text-light align-middle" href="https://github.com/italofds/find-router" target="_blank">find-router</a>
					<span class="badge rounded-pill text-bg-secondary align-middle ms-3" style="font-size:10pt;"><small>v1.0.0</small></span>
				</div>

				<div class="dropdown">
					<button class="btn btn-dark dropdown-toggle d-flex align-items-center" id="bd-theme" type="button" aria-expanded="false" data-bs-toggle="dropdown" data-bs-display="static" aria-label="Alterar Tema">
						<svg class="bi my-1 theme-icon-active"><use href="#circle-half"></use></svg>
						<span class="d-none ms-2" id="bd-theme-text">Alterar Tema</span>
					</button>
					<ul id="dropdown-theme" class="dropdown-menu dropdown-menu-end" aria-labelledby="bd-theme-text">
						<li>
							<button type="button" class="dropdown-item d-flex align-items-center" data-bs-theme-value="light" aria-pressed="false">
								<svg class="bi me-2 opacity-50"><use href="#sun-fill"></use></svg>
								Claro
								<svg class="bi ms-auto d-none"><use href="#check2"></use></svg>
							</button>
						</li>
						<li>
							<button type="button" class="dropdown-item d-flex align-items-center" data-bs-theme-value="dark" aria-pressed="false">
								<svg class="bi me-2 opacity-50"><use href="#moon-stars-fill"></use></svg>
								Escuro
								<svg class="bi ms-auto d-none"><use href="#check2"></use></svg>
							</button>
						</li>
						<li>
							<button type="button" class="dropdown-item d-flex align-items-center active" data-bs-theme-value="auto" aria-pressed="true">
								<svg class="bi me-2 opacity-50"><use href="#circle-half"></use></svg>
								Auto
								<svg class="bi ms-auto d-none"><use href="#check2"></use></svg>
							</button>
						</li>
					</ul>

					<svg xmlns="http://www.w3.org/2000/svg" class="d-none">
						<symbol id="check2" viewBox="0 0 16 16">
							<path d="M13.854 3.646a.5.5 0 0 1 0 .708l-7 7a.5.5 0 0 1-.708 0l-3.5-3.5a.5.5 0 1 1 .708-.708L6.5 10.293l6.646-6.647a.5.5 0 0 1 .708 0z"/>
						</symbol>
						<symbol id="circle-half" viewBox="0 0 16 16">
							<path d="M8 15A7 7 0 1 0 8 1v14zm0 1A8 8 0 1 1 8 0a8 8 0 0 1 0 16z"/>
						</symbol>
						<symbol id="moon-stars-fill" viewBox="0 0 16 16">
							<path d="M6 .278a.768.768 0 0 1 .08.858 7.208 7.208 0 0 0-.878 3.46c0 4.021 3.278 7.277 7.318 7.277.527 0 1.04-.055 1.533-.16a.787.787 0 0 1 .81.316.733.733 0 0 1-.031.893A8.349 8.349 0 0 1 8.344 16C3.734 16 0 12.286 0 7.71 0 4.266 2.114 1.312 5.124.06A.752.752 0 0 1 6 .278z"/>
							<path d="M10.794 3.148a.217.217 0 0 1 .412 0l.387 1.162c.173.518.579.924 1.097 1.097l1.162.387a.217.217 0 0 1 0 .412l-1.162.387a1.734 1.734 0 0 0-1.097 1.097l-.387 1.162a.217.217 0 0 1-.412 0l-.387-1.162A1.734 1.734 0 0 0 9.31 6.593l-1.162-.387a.217.217 0 0 1 0-.412l1.162-.387a1.734 1.734 0 0 0 1.097-1.097l.387-1.162zM13.863.099a.145.145 0 0 1 .274 0l.258.774c.115.346.386.617.732.732l.774.258a.145.145 0 0 1 0 .274l-.774.258a1.156 1.156 0 0 0-.732.732l-.258.774a.145.145 0 0 1-.274 0l-.258-.774a1.156 1.156 0 0 0-.732-.732l-.774-.258a.145.145 0 0 1 0-.274l.774-.258c.346-.115.617-.386.732-.732L13.863.1z"/>
						</symbol>
						<symbol id="sun-fill" viewBox="0 0 16 16">
							<path d="M8 12a4 4 0 1 0 0-8 4 4 0 0 0 0 8zM8 0a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 0zm0 13a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 13zm8-5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2a.5.5 0 0 1 .5.5zM3 8a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2A.5.5 0 0 1 3 8zm10.657-5.657a.5.5 0 0 1 0 .707l-1.414 1.415a.5.5 0 1 1-.707-.708l1.414-1.414a.5.5 0 0 1 .707 0zm-9.193 9.193a.5.5 0 0 1 0 .707L3.05 13.657a.5.5 0 0 1-.707-.707l1.414-1.414a.5.5 0 0 1 .707 0zm9.193 2.121a.5.5 0 0 1-.707 0l-1.414-1.414a.5.5 0 0 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .707zM4.464 4.465a.5.5 0 0 1-.707 0L2.343 3.05a.5.5 0 1 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .708z"/>
						</symbol>
					</svg>
				</div>
			</div>
		</header>

		<main class="flex-grow-1 overflow-auto position-relative">
			<div class="cover d-flex align-items-center" style="backdrop-filter: blur(10px);" v-if="mapMarkers.length == 0">
				<div class="container text-center text-light">
					<div class="alert alert-danger col-lg-6 mx-auto mb-3" role="alert">
						<strong>ATENÇÃO! </strong>Atualmente, a API do Google não está funcionando adequadamente para o tipo de aplicação dessa ferramenta. Em breve, serão feitos novos testes e ajustes.
					</div>					
					<h1 class="mb-3">Encontrar Roteador</h1>
					<p class="lead col-lg-6 mx-auto mb-5">Esta ferramenta recebe o endereço MAC de um ponto de acesso <em>Wi-Fi</em> e consulta um banco de dados de geolocalização para apresentar sua posição geográfica em um mapa interativo. Proporciona uma visualização precisa e rápida, sendo ideal para o rastreamento e a análise de dispositivos de rede.</p>
					<form @submit.prevent="handleFormSubmit" class="row justify-content-center" >
						<div class="col-lg-6 mx-auto">
							<div class="input-group">
								<input  v-maska data-maska="HH:HH:HH:HH:HH:HH" data-maska-tokens="H:[0-9a-fA-F]" v-model="macAddress" id="inputMacAddress" type="text" class="form-control form-control-lg text-center" placeholder="Endereço MAC" required="required">
								<button id="btnSearch" class="btn btn-primary btn-lg" type="submit">Buscar</button>
							</div>
							<div id="macAddressNotFound" class="invalid-feedback">
								Roteador não encontrado. Informe outro endereço MAC.
							</div>
						</div>						
					</form>
				</div>
			</div>

			<GMapMap ref="myMapRef" class="h-100" :center="mapCenter" :zoom="mapZoom" map-type-id="terrain" :options="mapOptions">
				<GMapMarker :key="marker" v-for="marker in mapMarkers" :position="marker.position" @click="openInfo()">
					<GMapInfoWindow :opened="isInfoOpened" :closeclick="true" @closeclick="hideInfo()">
						<div class="p-3">
							<h3 class="mb-2 text-dark">Roteador Localizado!</h3>
							<div class="mb-1 text-dark"><strong>Coordenadas (latitude/longitude):</strong></div>
							<div class="mb-3 text-dark">{{ mapCenter.lat }}, {{ mapCenter.lng }}</div>
							<a href="" @click="clearResult()">(Clique aqui pra realizar nova pesquisa)</a>
						</div>						
					</GMapInfoWindow>
				</GMapMarker>
				
			</GMapMap>
		</main>

		<footer class="flex-shrink-0 bg-body-tertiary">
			<p class="text-muted small text-center m-0">Desenvolvido por <a target="_blank" href="https://github.com/italofds">Ítalo Santos</a> | © 2024 | Licença GPL-3.0 | Hospedado pelo GitHub Pages | Contribua: <a target="_blank" href="https://github.com/italofds/find-router">github.com/italofds/find-router</a></p>	
		</footer>
	</div>
	
</template>

<script>
import axios from 'axios';
import darkMapStyleJSON from '../assets/dark-map-style.json'
import '../assets/js/color-modes.js';
import { vMaska } from "maska"

export default {
	name: 'App',
	directives: { maska: vMaska },
	data() {
		return {
			macAddress: '',
			mapMarkers: [],
			mapCenter: { lat: 0, lng: 0 },
			mapZoom: 2,
			mapOptions: {
				minZoom: 2,
				zoomControl: true,
				streetViewControl: false,
				fullscreenControl: false,
				mapTypeControlOptions: {
					position: 7
				},
			},
			isInfoOpened: true
		}
	},
	computed: {
	},
	methods: {
		openInfo() {
			this.isInfoOpened = true;
		},
		hideInfo() {
			this.isInfoOpened = false;
		},
		clearResult() {
			this.mapMarkers = [];
			this.mapCenter = { lat: 0, lng: 0 };
			this.macAddress = "";
		},
		async handleFormSubmit() {
			document.querySelector('#inputMacAddress').classList.remove("is-invalid");
			document.querySelector('#macAddressNotFound').classList.remove("d-block");


			const data = {
				"considerIp": "false",
				"wifiAccessPoints": [
					{
						"macAddress": "3c:37:86:5d:75:d4",
						"signalStrength": -35,
						"signalToNoiseRatio": 0
					},
					{
						"macAddress": this.macAddress,
						"signalStrength": -35,
						"signalToNoiseRatio": 0
					}
				]
			}

			try {
				var url  = "https://www.googleapis.com/geolocation/v1/geolocate?key=" + process.env.VUE_APP_MAPS_API_KEY;
				const response = await axios.post(url, JSON.stringify(data), {headers: {'Content-Type': 'application/json'}});

				const latitude = parseFloat(response.data.location.lat);
				const longitude = parseFloat(response.data.location.lng);

				if(latitude && longitude) {
					var marker = {
						position: {
							lat: latitude, lng: longitude
						},
					};
					this.mapMarkers.push(marker);

					this.mapCenter.lat = latitude;
					this.mapCenter.lng = longitude;
					this.mapZoom = 18;
				}
			
			} catch (error) {
				document.querySelector('#inputMacAddress').classList.add("is-invalid");
				document.querySelector('#macAddressNotFound').classList.add("d-block");

				console.error('Ocorreu um erro durante a busca dos dados: ', error);
			}	
		}
	},
	setup() {
		const mapStyle = darkMapStyleJSON;

		return {
			mapStyle
		}
	},
	mounted() {
		if(document.documentElement.getAttribute("data-bs-theme") === "dark"){
			this.mapOptions.styles = darkMapStyleJSON;
		}

		const mutationCallback = (mutationsList) => {
			for (const mutation of mutationsList) {
				if (
				mutation.type !== "attributes" ||
				mutation.attributeName !== "data-bs-theme"
				) {
				return
				}

				if(mutation.target.getAttribute("data-bs-theme") === "dark") {
					this.mapOptions.styles = darkMapStyleJSON;
				} else {
					this.mapOptions.styles = [];
				}
			}
		}
		const observer = new MutationObserver(mutationCallback);
		observer.observe(document.documentElement, { attributes: true });
	}
}
</script>

<style>
	.form-label {
		font-weight: bold;
	}
	.form-label:after {
		content: ":";
	}

	.bi {
		width: 1em;
		height: 1em;
		vertical-align: -.125em;
		fill: currentcolor;
	}

	.dropdown-menu .active .bi {
		display: block !important;
	}

	.navbar-brand:hover {
		text-decoration: underrow;
	}

	.navbar-brand a {
		text-decoration: none;
	}

	.navbar-brand a:hover {
		text-decoration: underline;
	}

	.navbar-icon {
		height: 20px;
	}

	.cover {
		position: absolute;
		width: 100%;
		height: 100%;
		background-color:rgba(0, 0, 0, 0.75);
		z-index: 1;
	}
</style>