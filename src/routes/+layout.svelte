<script>
	import favicon from '$lib/assets/favicon.svg';
	import CV from '$lib/assets/cv.pdf';
	import { Menu } from '@lucide/svelte';

	let { children } = $props();

	let name = $state("");
	let message = $state("");
	let email = $state("");

	let expand = $state(false);

</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div style="margin: 0 auto; height:100%; width:100%">
	<div class="show-normal">
	<nav>
		<div style="display: flex; justify-content: space-between; margin: 0 20px">
			<div>
				<div style="font-weight: bold; font-size:larger; margin-top: 20px;">Leonardo Ceragioli</div>
			</div>
			<ul>
				<li>
					<a href="/">Home</a>
				</li>
				<li>
					<a href="/talks">Talks</a>
				</li>
				<li>
					<a href="/writings">Writings</a>
				</li>
				<li>
					<a href="/work-in-progress">In Progress</a>
				</li>
				<li>
					<a href="/teaching">Teaching</a>
				</li>
				<li>
					<a href={CV} download>CV</a>
				</li>
				<li>
					<a href="#footer">Contact</a>
				</li>
			</ul>
		</div>
	</nav>
	</div>
	<div class="show-mobile">
		{#if !expand}
			<nav>
				<div style="display: flex; justify-content: space-between; margin: 0 20px;">
					<div>
						<div style="font-weight: bold; font-size:larger; margin-top: 20px;">Leonardo Ceragioli</div>
					</div>
					<div style="margin-top: 20px;">
						<button
						style="border: none; background-color:transparent; color:white;cursor:pointer;"
						onclick={() => expand = true}
						>
							<Menu />
						</button>
					</div>
				</div>
			</nav>
		{:else}
			<nav style:height="230px" style:transition="all 1s">
				<div style="display: flex; justify-content: space-between; margin: 0 20px">
					<div style="display: flex; flex-direction:column;">
						<div style="font-weight: bold; font-size:larger; margin-top: 20px;">Leonardo Ceragioli</div>
						<ul style="display: block; padding:0px;">
							<li>
								<div>
									<a href="/">Home</a>
								</div>
							</li>
							<li>
								<div>
									<a href="/talks">Talks</a>
								</div>
							</li>
							<li>
								<a href="/writings">Writings</a>
							</li>
							<li>
								<a href="/work-in-progress">In Progress</a>
							</li>
							<li>
								<a href="/teaching">Teaching</a>
							</li>
							<li>
								<a href={CV} download>CV</a>
							</li>
							<li>
								<a href="#footer">Contact</a>
							</li>
						</ul>
					</div>
					<div style="margin-top: 20px;">
						<button
						style="border: none; background-color:transparent; color:white;cursor:pointer;"
						onclick={() => expand = false}
						>
							<Menu />
						</button>
					</div>
				</div>
			</nav>
		{/if}
	</div>
	{@render children?.()}

	<div class="footer" id="footer">
		<div style="margin: 0 30px; display: flex; flex-direction: column;">
			<h2 style="color: white;">Contact:</h2>
			<h4>
        		<a href="https://unipi.academia.edu/LCeragioli" target="_blank"> My Academia page </a>
        	</h4>
			<h4>
        		<a href="https://www.researchgate.net/profile/Leonardo-Ceragioli-2" target="_blank"> My ResearchGate page </a>
        	</h4>
			<h4>
				<a href="mailto:leo.crg.uni@gmail.com">leo.crg.uni@gmail.com</a>
			</h4>
		</div>
		<div style="margin: 0 30px; display: flex; flex-direction: column;">
			<h2 style="color: white;">Groups:</h2>
			<h4>
            	<a href="https://luci.unimi.it/" target="_blank"> LUCI Lab </a>
        	</h4>
			<h4>
            	<a href="https://sites.unimi.it/smartest/" target="_blank"> SMARTEST </a>
        	</h4>
			<h4>
            	<a href="https://www.youtube.com/@gavagaiphi" target="_blank"> Gavagai student association (YouTube page) </a>
        	</h4>
		</div>
		<!-- <div 
		style="display: flex; flex-direction: column; margin: 0 30px; width: 20%;"
		>
			<h2 style="color: white;">Message me:</h2>
			<label for="title" style="color: white">Name:</label>
			<input id="title" bind:value={name} />
			<label for="message" style="color: white">Message:</label>
			<textarea id="message" rows="5" bind:value={message}></textarea>
			<label for="email" style="color: white">Email:</label>
			<input id="email" bind:value={email} />
			<button>send</button>
		</div> -->
	</div>
</div>
	
	
<style>

ul {
	display: flex;
	list-style: none;
}

li {
	margin-left: 20px;
}

a:hover {
	color: rgb(189, 189, 189);
}

.show-mobile {
	display: none;
}

.show-normal {
	display: contents;
}

nav {
	top: 0;
	position: sticky;
	overflow: hidden;
	background-color: rgb(110, 160, 110);
	color: white;
}

a {
	color: white;
}

.footer {
	bottom: 0;
	width: 100%;
	height: 100%;
	left: 0;
	background-color: rgb(110, 160, 110);
	display: flex;
	justify-content: space-between;
}


.footer input {
	border-radius: 2px;
	padding: 5px;
	margin-bottom: 10px;
}

.footer textarea {
	overflow: hidden;
	border-radius: 5px;
	padding: 5px;
	margin-bottom: 10px;
}

.footer button {
	overflow: hidden;
	width: 50%;
	align-self: center;
	text-align: center;
	border-radius: 20px;
	padding: 5px;
}

@media screen and (max-width: 540px) {
	.show-normal {
		display: none;
	}

	.show-mobile {
		display: contents;
	}

	nav {
		top: 0;
		position: sticky;
		overflow: hidden;
		background-color: rgb(110, 160, 110);
		color: white;
	}

	li {
		margin: 0;
		margin-bottom: 5px;
	}
}

</style>
