<script>
	import { crossfade, scale } from 'svelte/transition';
    import Button from "@smui/button"

    const [send, receive] = crossfade({
		duration: 200,
		fallback: scale
	});
    let selected = null;


let projects = [
    {id: 1, title:"Artworld", company: "Stichting de vrolijkheid", discription: `
<p>Introducing the Digital Art World video game - a revolutionary platform that has captured the hearts and minds of over 3000 refugee kids. This innovative game offers an unparalleled opportunity for children to express themselves through drawing, stop-motion animation, and music, all while having fun and learning new skills.</p>

<p>The goal of the game is simple yet profound - to inspire and motivate kids to create art. With the Digital Art World game, children are given the tools and resources they need to unleash their creativity and explore their artistic potential. They can draw, animate, and compose music to their hearts' content, all within a safe and engaging virtual environment.</p>

<p>The game's impact has been nothing short of remarkable. Workshops have been held in over 16 refugee camps throughout the Netherlands, and the response from kids has been overwhelmingly positive. Children are excited to participate in the game, and their enthusiasm is infectious. In fact, some kids are so eager to continue playing that they have been known to sneak back into the game through windows, long after the workshops have ended.</p>

<p>It's no surprise that the Digital Art World game has been such a success. After all, it was crafted with care and attention to detail over a two-year period. The game was built using cutting-edge technologies, including Svelte, PhaserJS, and Nakama. On the front end, JavaScript was used to power the game's dynamic user interface, while the back end was built using the robust and efficient Go programming language.</p>

<p>The Digital Art World video game represents a new frontier in digital art and education. With its engaging gameplay, powerful tools, and enthusiastic community of young creators, it is poised to change the way we think about creativity and learning. So why not join the fun and discover the magic of the Digital Art World video game for yourself?</p>
    `, url: "https://vimeo.com/779619037", img: "./projects/artworld.webp"},
    {id: 2, title:"Like dust", company: "Sam Yazdanpanna", discription: `
    <p>Introducing "Like Dust", an interactive graphic novel that tells a powerful and poignant story of a young boy who was forced to flee his home country. Created using the cutting-edge Svelte technology, this incredible piece of art was coded in just one week.</p>

<p>The story of "Like Dust" is one that is shared by thousands of children worldwide - a story of pain, loss, and resilience. It's a story that needs to be told, and "Like Dust" does so in a way that is both beautiful and impactful.</p>

<p>The interactive nature of this graphic novel is what truly sets it apart. The viewer is invited to immerse themselves in the story, to explore the world and the characters in a way that is both engaging and enlightening. The experience is fully responsive, meaning that it can be accessed and enjoyed on desktop, Android, and iPhone devices, making it accessible to as many people as possible.</p>

<p>"Like Dust" is a testament to the power of art and storytelling. Through its stunning visuals and powerful narrative, it offers a unique perspective on the world and the challenges that so many people face. It's a work of art that deserves to be celebrated and shared, and we can't wait to see what its creator will come up with next.</p>

<p>So why not take a moment to experience "Like Dust" for yourself? Let yourself be transported to a world of beauty, pain, and hope, and discover the power of interactive storytelling in a way that you've never experienced before.</p>
    `, url: "https://likedust.nl", img: "./projects/likedust.webp"},
    {id: 3, title:"Price calculator", company: "De betonboorder", discription: `
    <p>Introducing the Price Calculation Tool made for Debetonboorder - the company that drills holes through concrete and everything that comes with it. With their expertise and professionalism, Debetonboorder has become a household name in their industry, but with success comes a lot of attention.</p>

<p>Debetonboorder was being bombarded with calls and emails from clients, which made it difficult to manage the workload effectively. To simplify the process and to give their clients more flexibility, they asked me to create a price calculation tool that allows clients to calculate the cost of their project themselves. This tool offers an easy and user-friendly interface that provides a complete overview of all the costs involved.</p>

<p>By using the price calculation tool, the end-user can easily input their project's details, including the size, location, and other important factors. The tool then provides an accurate estimate of the project's cost, making it easy for the client to understand and plan accordingly. Once the project has been calculated, the invoice is sent directly to the client and the company via email. This feature saves time and ensures that the request is structured correctly, and photos can be added when needed.</p>

<p>The Price Calculation Tool is a game-changer for Debetonboorder. It not only provides a hassle-free experience for their clients but also allows them to focus on the most important aspects of their work. This tool has streamlined their workflow, making it easier to manage requests, and has significantly reduced the workload for the company.</p>

<p>With the introduction of the Price Calculation Tool, Debetonboorder has set the bar high in their industry. It is an excellent example of how technology can be used to create a better experience for both the company and the clients. The tool's ease of use, accuracy, and flexibility has made it a valuable asset, and we can't wait to see how Debetonboorder continues to innovate and improve their services.</p>

    `, img: "./projects/debetonboorder.webp", url: "https://debetonboorder.nl/prijscalculator"},
    {id: 4, title:"Webshop & videocourse platform", company: "Robijn Tilanus", discription: `
    <p>I am  happy to introduce the latest upgrade to Robijn Tilanus' website, a cutting-edge online platform that showcases her unique approach to teaching improvisation within music. me and my coleague, Tim have used tools such as WordPress, WooCommerce, and LearnDash and a custom theme that not only meets but exceeds the latest standards in wordpress development.</p>

<p>The new theme is designed to provide an intuitive and user-friendly experience for visitors, with a sleek and modern design that is fully responsive across all devices. It is also built with the latest WordPress block editor, Gutenberg, which provides a range of customization options to make the website truly unique.</p>

<p>To ensure maximum performance and reliability, the website is hosted on a custom VPS that is optimized for speed and stability. This means that visitors can enjoy lightning-fast loading times, without any downtime or performance issues.</p>

<p>One of the key features of Robijn Tilanus' website is her range of offerings, which include books, video courses, and workshops. With the new website upgrade, visitors can now browse and purchase these products with ease, thanks to the integration of WooCommerce. This feature provides a seamless shopping experience, with secure payment processing and efficient order management.</p>

<p>Robijn Tilanus has gained large amounts of traffic from across the globe, thanks to her unique teaching methods and engaging content. Visitors are captivated by her passion for improvisation and her ability to communicate complex concepts in a simple and approachable way.</p>

<p>Overall, the new website upgrade is a testament to our commitment to excellence in web development. We are proud to have played a part in helping Robijn Tilanus share her knowledge and passion with the world, and we look forward to seeing her continued success in the future.</p>
    `, url: "https://robijntilanus.nl", img: "./projects/robijntilanus.webp"},
    // {id: 5, title:"CardChat", company: "Lindsey Schaap", discription: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.", url: "https://cardchat.app", img: "./projects/cardchat.webp"},
    {id: 6, title:"Online Newspaper", company: "Oost-online", discription: `
    <p>I am excited to have been working with Oost Online, a friendly newspaper that provides readers with up-to-date news and information about everything that's happening in the East of Amsterdam. I have been hosting the website for many years, ensuring that it is always up and running, no matter how much traffic it receives.</p>

<p>In recent months, me and other freelancers I work with, have undertaken a major upgrade of the website to ensure that it is fully updated and optimized for performance. This includes creating a custom child theme that reflects Oost Online's unique brand and identity, while providing users with a seamless and intuitive browsing experience.</p>

<p>Our team has worked tirelessly to ensure that the website is fully optimized for speed, security, and reliability, using the latest technologies and techniques in web development. We have also implemented a range of advanced features, such as social media integration, to make it easy for readers to share and engage with Oost Online's content.</p>

<p>Thanks to our efforts, Oost Online's website is now fully equipped to handle the huge influx of traffic that some of its articles can generate, without any downtime or performance issues. This means that readers can always rely on Oost Online to provide them with timely and accurate news and information, no matter what's happening in the East of Amsterdam.</p>

<p>Overall, we are proud to have played a part in helping Oost Online reach its audience and achieve its goals. Our commitment to excellence in web development, combined with our deep understanding of Oost Online's unique needs and requirements, has enabled us to deliver a website that is both powerful and user-friendly, ensuring that readers can always stay informed and engaged with the news and events of their community.
  </p>  `, url: "https://oostonline.nl", img: "./projects/oostonline.webp"},
]

/**
	 * @param {{ title: string; company: string; discription: string; url: string; img: string; }} project
	 */
function openModal(project){
    console.log(project)
    selected = project
}
</script>

<div class="projects" id="projects">
    <h1>Recent projects</h1>
    <div class="container">
    {#each projects as project }
        {#if selected !== project}
        <img  
            on:click="{()=>{openModal(project)}}" 
            in:receive={{key:project.id}}
            out:send={{key:project.id}}
            class="projectImg" src="{project.img}" alt="{project.title}"
        >
        {/if}
    {/each}

    
    </div>
    {#if selected !== null}
        {#await selected then project}
        <div class="modalFrame" on:click={()=>{selected = null;}}>
            <div class="modal" on:click|stopPropagation="{()=>{}}" in:receive={{key:project.id}} out:send={{key:project.id}}>
                <div class="close" on:click={()=>{selected = null;}}>x</div>
                <img src="{project.img}" alt="{project.title}" >
                <!-- <h1>{project.title}</h1>
                <h2>{project.company}</h2> -->
                <p>{@html project.discription}</p>
                <a href="{project.url}" target=”_blank”><button>check out project</button></a>
            </div>
        </div>
        {/await}
    {/if}
</div>


<style>

    .projectImg {
        max-width: 650px;
        margin: 20px;
        box-shadow: 5px 5px 10px gray;
    }

    .projectImg:hover {
        box-shadow: 5px 5px 25px gray;
        cursor: pointer;
    }

    .projects {
        background-color: #e5e6ff;
        padding: 50px;
    }  
   
    .card-container {
       max-width: 250px;
       margin: 15px;
    }

    img {
        width: 100%;
    }
    p {
        padding: 25px;
    }

    .modal {
        max-width: 1024px;
        margin: 30px;
        background: white;
        box-shadow: 0 0 30px gray;
        position: relative;
        overflow-y: auto;
    }
   
    .modalFrame {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        z-index: 15;
        backdrop-filter: blur(5px);
    }

    .close {
        margin: 10px;
        font-size: 40px;
        z-index: 10;
        position: absolute;
        right: 10px;
        top: 10px;
        color: white;
        cursor: pointer;
    }
</style>