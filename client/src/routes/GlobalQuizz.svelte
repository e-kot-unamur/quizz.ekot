<script>
    import QuizzArea from "../components/quizzComponents/QuizzArea.svelte";
    export let index;
</script>

<style>  
    .quizzArea {
        min-height: 100vh;
    }
    body {
        background-color: #609d9f;
        border : 1px solid #609d9f;
    }

    /* Cercle */
    .cercle {
        position: absolute;
        display: block;

        animation-name: changeColorAndPlaceCercle;
        animation-duration: 8s;
        animation-iteration-count: infinite;  
        animation-direction: alternate ;
        animation-timing-function: ease;
    }

    @keyframes changeColorAndPlaceCercle {
        0%   {fill:#8DE7EB; left:5%; top:10%; height: 30%;}
        25%  {left:5%; top:11%;}
        50%  {left:6%; top:11%;}
        75%  {left:6%; top:11%;}
        100% {fill:#67A9AB; left:6%; top:11%; height: 35%;}
    }

    /* Rectangle */
    .rectangle {
        position: absolute;
        display: block;

        animation-name: changeColorAndPlaceRectangle;
        animation-duration: 10s;
        animation-iteration-count: infinite;  
        animation-direction: alternate ;
        animation-timing-function: ease;
    }

    @keyframes changeColorAndPlaceRectangle {
        0%   {fill:#5EAB82; left:75%; top:70%; height: 95%; transform: rotate(45deg)}
        25%  {left:73%; top:69%;}
        50%  {left:73%; top:69%;}
        75%  {left:73%; top:68%;}
        100% {fill:#64B5A1; left:70%; top:68%; height: 100%; transform: rotate(40deg)}
    }

    /* Logos */ 
    .logoEkot {
        position: absolute;
        display: block;

        width : 8%;
        top : 20px;
        left : 90%;
    }

    .logoHome {
        width: 50px;
        position: fixed;
        top : 20px;
        left: 20px;
    }
    
    /* Mobile first */
    @media (max-width : 850px) {
        .logoEkot {
        width : 12%;
        top : 10px;
        left : 81%;
        }

        .logoHome {
            top : 15px;
            left: 10px;
        }
    }
</style>

<body>
    <!-- Zone du Quizz -->
    <div class="quizzArea">
        <a href="/"><img src="/svg/close.svg" alt="Logo E-kot" class="logoHome" /></a>

        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" class="cercle">
            <circle cx="50" cy="50" r="50"/>
        </svg>

        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" class="rectangle">
            <rect width="100%" height="100%" />
        </svg>

        <img src="/svg/logo_blanc.svg" alt="Logo E-kot" class="logoEkot"/>

        <QuizzArea index = {index}/>
    </div>
</body>