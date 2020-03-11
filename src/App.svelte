<script>

	import StatRow from "./UI/StatRow.svelte";
	import Navbar from "./UI/Navbar.svelte";
	import Resource from "./UI/Resource.svelte";
	import StatCluster from "./UI/StatCluster.svelte";
	import StatContainer from "./UI/StatContainer.svelte";
	import Portrait from "./UI/Portrait.svelte";
	import StatResource from "./UI/StatResource.svelte";
	import Description from "./UI/Description.svelte";

	export let url = "";

	export let resources = [

		{
			name: "Corpus",
			max: "100",
			value: "66",
			abbr: "CPT",
			id: "corpus"
		},
		{
			name: "Animus",
			max: "100",
			value: "66",
			abbr: "APT",
			id: "animus"
		},
		{
			name: "Spiritus",
			max: "100",
			value: "66",
			abbr: "SPT",
			id: "spiritus"
		}

	];

	export let statResources = [

		{
			name: "Health",
			value: 12,
			max: 24,
			id: "health"
		},
		{
			name: "Congruence",
			value: 12,
			max: 24,
			id: "congruence"
		},
		{
			name: "Willpower",
			value: 12,
			max: 24,
			id: "willpower"
		},
		{
			name: "Armour",
			value: 12,
			max: 24,
			id: "armour"
		}

	]

</script>

<style>


	#desc-magic {
		display: inline-flex;
		flex-direction: column;
	}

	.stat-resource {
		display: inline-flex;
		flex-wrap: nowrap;
		flex-grow: 1;
		flex-direction: column;
		padding: 1px;
		margin: 2%;
		background-color: rgba(207, 173, 116, 0.8);
	}

	:global(body), :global(html) {
		margin: 0;
		padding: 0;
		width: 100%;
		overflow: hidden;
		min-width: fit-content;
		background-color: rgba(119, 136, 170, 0.6);
	}

	:global(.primary-stat-div) {
		background-color: rgba(150, 122, 75, 0.9);
		display: inline-flex;

	}

	.stat-and-chat-container {
		display: flex;
		margin: 10px 0 0 0;
		transform: scale(1.5);
		transform-origin: 0 0;
		/*flex-wrap: wrap;*/
	}

	.super-super-stat-container {
		display: inline-table;
		flex-wrap: wrap;
		/* flex: 1 1 300px; */
	}

	#triad-container {
		display: inline-flex;
	}


	.super-stat-container-top {
		display: flex;
		flex-wrap: wrap;
		margin: 27px 0 0 0;
	}

	.super-stat-container {
		display: inline-flex;
		flex-wrap: nowrap;
		margin: 0;
	}

	.stat-container {
		display: inline-flex;
		flex-wrap: wrap;
		flex-grow: 1;
		/* padding: 1px; */
		/* margin: 1px; */
		/* background-color: rgba(167, 119, 44, 0.7); */
	}

	#top-stat-container {
		flex-direction: column;
		flex-wrap: wrap;
	}

	.navigation-bar-sticky {
		position: fixed;
		width: 100%;
		background-color: rgba(235, 213, 179, 0.8);
		margin: 0;
		padding: 0;
		top: 0;
		border-bottom: solid #776b5b;
		z-index: 2;
	}


	.stat-2-container {
		display: inline-flex;
		max-width: fit-content;
		margin: 25px 0 0 0;
	}

	.stat-2-box {
		display: inline-flex;
		flex-direction: column;
		flex-wrap: wrap;
		/*background-color: #186A3B;*/
	}

	#stat-resources {
		display: inline-flex;
		flex-direction: row;
		width: fit-content;
	}



</style>

<body>

<div class="navigation-bar-sticky">

<Navbar/>

</div>

<div class="stat-and-chat-container">

	<div class="super-super-stat-container">

		<section class="super-stat-container-top">

			<article id="top-stat-container" class="stat-container">


						<div id="stat-resources">

							<Portrait  />

							{#each resources as array}
								<Resource  name="{array.name}" value="{array.value}" abbr="{array.abbr}" max="{array.max}" id="{array.id}" />
							{/each}

						</div>



				<div id="triad-container" class="stat-container">

					<StatRow/>

				</div>

			</article>


		</section>

		<section class="super-stat-container">

			<StatContainer/>


		</section>

	</div>

	<section class="stat-2-container">
		<article class="stat-2-box">

			<div class="stat-container">

				<div class="stat-resource">

					{#each statResources as array}
					<StatResource name="{array.name}" max="{array.max}" value="{array.value}" id="{array.id}" />
					{/each}

				</div>





				<div class="stat-container" id="desc-magic">

					<StatCluster/>

					<Description />


				</div>




			</div>

		</article>
	</section>

</div>







</body>

<!--<Resource />-->
<!--<StatRow  />-->
<!--<StatResource />-->
<!--<StatCluster />-->
<!--<StatResource />-->
<!--<StatCluster />-->
<!--<StatContainer />-->