<script lang="ts">
	import thomannImage from '$lib/assets/images/partners/thomann.webp';
	import ueberschallImage from '$lib/assets/images/partners/ueberschall.webp';
	import sparkasseImage from '$lib/assets/images/partners/sparkassekoelnbonn.webp';
	import esiImage from '$lib/assets/images/partners/esi.webp';
	import nrwInklusionImage from '$lib/assets/images/partners/inklusionsscheck.webp';
	import aktionMenschImage from '$lib/assets/images/partners/Aktion_Mensch_Logo.svg';
</script>

<ul class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-4">
	<li class="flex justify-center items-center p-2">
		<img class="max-h-16 object-contain" src={thomannImage} alt="Musikhaus Thomann" />
	</li>
	<li class="flex justify-center items-center p-2">
		<img class="max-h-16 object-contain" src={ueberschallImage} alt="Ueberschall" />
	</li>
	<li class="flex justify-center items-center p-2">
		<img class="max-h-16 object-contain" src={sparkasseImage} alt="Sparkasse Köln Bonn" />
	</li>
	<li class="flex justify-center items-center p-2">
		<img class="max-h-16 object-contain" src={esiImage} alt="ESI" />
	</li>
	<li class="flex justify-center items-center p-2">
		<img
			class="max-h-16 object-contain"
			src={nrwInklusionImage}
			alt="NRW inklusiv - Inklusionsscheck"
		/>
	</li>
	<li class="flex justify-center items-center p-2">
		<img class="max-h-16 object-contain" src={aktionMenschImage} alt="Aktion Mensch" />
	</li>
</ul>
