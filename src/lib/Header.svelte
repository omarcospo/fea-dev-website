<script lang="ts">
	import ondasGif from '/images/ondas.gif';
</script>

<main>
	<div class="ondas_container">
		<img class="ondas" src={ondasGif} alt="Elemento gráfico de ondas" />
		<div class="heading_ondas">
			<h1>FEA.dev</h1>
			<p>
				Somos a primeira organização estudantil focada em programação na FEA-USP (Faculdade de
				Economia, Administração, Contabilidade e Atuária da Universidade de São Paulo).
			</p>
			<button class="button">Saiba mais</button>
		</div>
	</div>
</main>

<style>
	.ondas_container {
		position: relative;
		overflow: hidden;
	}
	.ondas {
		width: 100%;
		height: 30em;
		object-fit: cover;
	}
	.heading_ondas {
		position: absolute;
		z-index: 2;
		top: 25%;
		left: 5%;
	}
	.heading_ondas p {
		width: 40%;
		margin-top: -1em;
	}
	/* --- mobile */
	@media (max-width: 768px) {
		.ondas {
			width: 140%;
			height: 17em;
		}
		.heading_ondas {
			top: 11%;
			font-size: 0.8em;
		}
		.heading_ondas p {
			width: 60%;
		}
	}
</style>
