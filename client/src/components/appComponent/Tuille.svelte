<script>
    export let src;
    export let route;
</script>

<style>
    .tuille {
        display : block;
        margin: 10px auto 20px auto;
        border : 1px solid #8DE7EB;
        width : 50%;
        padding: 10px 25px;
        background-color: #D3EAEB;
        text-decoration: none;
    }

    a {
        color: #000;
        text-decoration: none;
    }

    a:hover {
        text-decoration: none;
        color: black;
    }

    .image {
        display: block;
        margin: auto;
        width : 90%;
    }

    .nomDuQuizz {
        text-align: center;
        color : #8D6F9E;
        margin-bottom: 0;
    }

    .proposeBy {
        display: flex;
        justify-content: end;
        margin: 0;
    }

    @media (max-width : 780px) {
        .tuille {
            width: 90%;
        }
        
        .proposeBy {
            justify-content: center;
        }
    }
    
</style>

<div class="tuille" >
    <a href="{route}">
        <!-- Titre -->
        <div class="">
            <h1 class="nomDuQuizz">
                <slot name="title">
                    <span>Oups... Erreur titre</span>
                </slot>
            </h1>
        </div>

        <!-- Image -->
        <div class="">
            <img {src} alt="Illustration quizz" class="image"/>
        </div>
    
        <!-- Proposé par -->
        <div class="proposeBy"> by &#129;
            <slot name="proposeBy">
                <span>Proposé par "undefined"</span>
            </slot>
        </div>
    </a>
</div>