<script>
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';

	let carousel;
	const users = [


        {
			name: 'Lloyd Chambrier',
			title: 'Colleague',
			img: 'https://media.licdn.com/dms/image/C4E03AQG_VCddVBypjA/profile-displayphoto-shrink_200_200/0/1631008371233?e=1687392000&v=beta&t=z-SYHWnYdm1TAdTcsQvUqWkzCC-B7Ipw684npe0VDlM',
			text: `<p>Lindsey has a strong knowledge in Javascript, Node.js, Wordpress and PHP.</p>

<p>I have consulted him for a variety of projects and his skills and insights have always been invaluable. He's very good at identifying problems fast and finding the most efficient solutions for those as well.</p>

<p>I can definitely recommend working with him or having him on your team.</p>`
		},
		{
			name: 'Maarten van der Glas',
			title: 'Colleague',
			img: 'https://media.licdn.com/dms/image/C4E03AQHz_jETVka5ww/profile-displayphoto-shrink_200_200/0/1517683733314?e=1687392000&v=beta&t=lbCRlq6KcCQ81NWjKGpAKyky0iZZUzrjY9wCHhoKrRQ',
			text: `<p>Lindsey has a broad understanding of HTML, CSS, and many different Javascript libraries/ frameworks. With his deep knowledge he works fast, and is quick in learning a new framework or API.</p>

<p>Lindsey also has good experience with backend development and server admin: docker, database management, and linux.</p>

<p>This makes Lindsey a good team member, when someone with broad skills is needed.</p>

<p>Lindsey is willing to go the extra mile for the project.</p>`
		},
		{
			name: 'Dan Gibbon-walsch',
			title: 'Client',
			img: 'https://media.licdn.com/dms/image/C5603AQHIovHYggOO0g/profile-displayphoto-shrink_100_100/0/1591268423081?e=1687392000&v=beta&t=VRhdcx4ib5yU9SitX17HjPFLUazFap9SMzR-sKPKwQ0',
			text: 'Lindsey offers a really interesting take on combining current technology, fun education material and how to equip people for skills of the future. Really recommend working with him!'
		},
        {
			name: 'Ilse van der glas',
			title: 'Client',
			img: 'https://media.licdn.com/dms/image/C5603AQFBcrejNbgIPA/profile-displayphoto-shrink_100_100/0/1517690996793?e=1687392000&v=beta&t=YfOpvH6JS7gLnWafgGmMmDJYe2d7gAB048iSZSa_Gok',
			text: 'Lindsey is a very driven and nice personality. Open to learn and teaches a lot. Recommended to hire!'
		}
	];
</script>

<div class="testamonials">
	<h1>What others say</h1>
	<div class="container">
		{#if browser}
			<Carousel bind:this={carousel}>
				{#each users as user}
					<div class="review">
						<p>{@html user.text}</p>
						<img alt="user.name" src={user.img} />
						<h4>{user.name}</h4>
						<h2>{user.title}</h2>
					</div>
				{/each}
			</Carousel>
		{/if}
	</div>
</div>

<style>
	.testamonials {
		background-color: #ffd5bc;
		padding: 50px;
	}

	.review {
        text-align: center;
        display: flex;
        justify-content: center;
        flex-direction: column;
	}

    .review p {
        max-width: 800px;
        margin: 15px auto;
        font-size: 25px;
    }

    .container {
        margin: 50px auto;
        max-width: 1024px;
    }

    :global(.sc-carousel-arrow__circle) {
        width: 50px!important;
        height: 50px!important;
    }

    img {
        width: 125px;
        margin: 0 auto;
    }
</style>
