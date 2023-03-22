<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import me from '$lib/images/me.jpg';
</script>

<svelte:head>
	<title>Portfolio</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
		<span class="welcome">
				<img src={welcome} alt="Welcome" />
		</span>
		<h1>Vladimir's Zelenokor Website</h1>
		<h2>My personal portfolio </h2>   
        
	<div style="display:-ms-flexbox; display:flex">

		<div style="-ms-flex: 70%; flex: 70%; padding:10px;background-color: #1111;">
			<h3>About Me:</h3>

			<p>
				Hello, I am Vladimir Zelenokor. I am a student of Innopolis University. I am 20 years old and i was boarn in Chelyabinsk. My main job is sound engineering. I write music in different genres and sell it to people, but I also mix and master vocals. The main genres I work with are hip-hop, rnb, electronic music.
			</p>

			<h3 >My background and exprerience in area:</h3>

			<div>
				<p>
					I have been fond of music for about 5 years, but I started studying 1.5 years ago. During these 1.5 years I managed to:
				</p>
		
				<ol>
					<li>pass several paid courses that increased my qualifications:</li>
					<ul>
						<li>IY beatmaker's course</li>
						<li>weak of workshops from "Фонтанка studio"</li>
					</ul>
					<li>open community for the sale of music. service:</li>
					<ul>
						<li>saling beats</li>
						<li>mixing vocals</li>
					</ul>
					<li>interactу with much popular producers to create unique content:</li>
					<ul>
						<li>YG Woods</li>
						<li>@curlygotcha</li>
					</ul>
					<li>find dozens of clients and make sellings</li> 
				</ol>
			</div>
		</div>

		<div style="-ms-flex:30%; flex: 30%; padding:3%">
			<img style="height:max-content; width: 100%; display: block;border-radius: 50%;" src={me} alt="">
		</div>
    </div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
	img{
            height: 30px;
            width: 30px;
        }
</style>
