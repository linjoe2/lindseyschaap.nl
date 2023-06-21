<script>

</script>

<div class="skills" id="skills">
    <div class="blur">
        <h1>Top skills</h1>
        <div class="imageBox">
            <img src="./skillIcons/html-5.png" alt="html"/>
            <img src="./skillIcons/css-3.png" alt="css"/>
            <img src="./skillIcons/js.png" alt="js" />
            <img src="./skillIcons/svelte.png" alt="svelte" />
            <img src="./skillIcons/wordpress.png" alt="wordpress" />
            <img src="./skillIcons/docker.png" alt="docker" />
            <img src="./skillIcons/linux.png" alt="linux" />
            <img src="./skillIcons/github.png" alt="github" />
        </div>
    </div>
</div>


<style>

    .skills {
        background-image: url(/backgrounds/code.webp);
        box-shadow: 0px 0px 30px black;
        color: white;
        /* background-attachment: fixed; */
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        z-index: 1;
    }

    .blur {
        backdrop-filter: blur(5px) grayscale(0.7);
        -webkit-backdrop-filter: blur(5px) grayscale(0.7);
        padding: 20px;
    }

    .imageBox {
        display: flex;
        justify-content: space-around;
        max-width: 1024px;
        margin: 20px auto;
        width: 100%;
        flex-wrap: wrap;
    }

    img {
        width: 75px;
        margin: 10px;
    }
</style>