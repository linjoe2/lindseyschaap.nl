<script>

</script>

<div id="hero" class="container">
    <div id="headshot">
        <img src='./headshot.webp' alt="headshot" id="headshot"/>

    </div>
    <div id="heroText">
        <h3>Full stack web developer and Digital educator </h3>
        <a href="#projects"><button>view projects</button></a>
        <a href="#skills"><i class="arrow down"></i></a>
    </div>
    
</div>


<style>

    #hero {
        height: 100vh;
        display: flex;
        justify-content: center;
        flex-direction: column;
    }
    
    #headshot {
        max-width: 250px;
        margin: 0 auto;
        display: block;
        }

    #heroText{
        text-align: center;
    }

    .arrow {
        border: solid black;
        border-width: 0 5px 5px 0;
        display: inline-block;
        padding: 5px;
    }

    .down {
        transform: rotate(45deg);
        -webkit-transform: rotate(45deg);
        -webkit-animation: mover 2s infinite  alternate;
        animation: mover 2s infinite  alternate;
    }

    @-webkit-keyframes mover {
    0% { transform: translateY(0) rotate(45deg);  }
    100% { transform: translateY(-15px) rotate(45deg); }
    }
    @keyframes mover {
        0% { transform: translateY(0) rotate(45deg); }
        100% { transform: translateY(-15px) rotate(45deg); }
    }
</style>