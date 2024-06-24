<template>
<!-- First section "HEADER" -->
<header>
    <div class="container">
        <div class="wrapper">
            <div class="infobox">
                <img src="@/assets/main-image.png" alt="">
                <p class="subheading">Aprenda as linguagens HTML e CSS do zero e crie sites incríveis sem precisar saber programar!</p>
                <h1 class="neo-sans">Inscreva-se agora e garanta:</h1>
                <ul class="list">
                    <li class="items">
                        <i class="bi bi-check-circle-fill"></i>
                        <span class="text-light">Desconto especial de lançamento: de R$ 497,00 por apenas R$ 197,00!</span>
                    </li>
                    <li class="items">
                        <i class="bi bi-check-circle-fill"></i>
                        <span class="text-light">Pagamento facilitado em até 12 parcelas de R$ 15,09.</span>
                    </li>
                    <li class="items">
                        <i class="bi bi-check-circle-fill"></i>
                        <span class="text-light">Bônus exclusivos, como e-book gratuito e modelos prontos para usar.</span>
                    </li>
                    <li class="items">
                        <i class="bi bi-check-circle-fill"></i>
                        <span class="text-light">Acesso imediato às aulas e materiais do curso.</span>
                    </li>
                </ul>
            </div>
            <figure class="illustrative">
                <img src="@/assets/ilustrative-image.png" alt="">
                <a href="#" rel="noopener" class="main-cta">INSCREVA-SE AGORA</a>
            </figure>
        </div>
    </div>
    <img src="@/assets/separator.png" class="separator">
</header>
<!-- / End First Section "HEADER" -->
</template>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');
@import url('https://fonts.cdnfonts.com/css/neo-sans-std');

body {
    background: #141933 !important;
    color: #FFF !important;
    font-family: 'Open Sans', sans-serif !important;
}

/* Personalizando a barra de rolagem */
::-webkit-scrollbar {
    width: 3px;
    background-color: #141933;
}

::-webkit-scrollbar-thumb {
    background-color: #952AFF;
    border-radius: 5px;
}

::-webkit-scrollbar-track {
    background-color: #fff;
}

/*
    First section "Header Section"
*/
.wrapper {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    padding-top: 100px;
}

.wrapper .infobox {
    display: table;
}
.wrapper .infobox {
    width: 70% !important;
}

.subheading {
    color: #FFF;
    font-family: 'Open Sans', sans-serif;
    font-size: 1.2rem;
    font-weight: 500;
    line-height: 1.7;
    margin-top: 30px;
}

h1.neo-sans {
    color: #FFC32A;
    font-size: 1.5rem;
    font-family: 'Neo Sans Std', sans-serif;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

ul.list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 10px;
    width: 100%;
}
li.items {
    display: flex;
    align-items: center;
    gap: 7px;
    font-family: 'Open Sans', sans-serif;
    font-size: 1rem;
    font-weight: 500;
}

.illustrative {
    width: 30%;
    min-width: 300px;
    display: table;
    text-align: center;
}

.illustrative img {
    width: 100%;
    height: auto !important;
}
.illustrative a.main-cta {
    text-decoration: none;
    color: #FFF;
    font-size: 1.3rem;
    font-family: 'Open Sans', sans-serif;
    font-weight: 500;
    display: table;
    padding: 14px 30px;
    border-radius: 15px;
    background: #952AFF;
    box-shadow: 3px 3px 30px rgba(0, 0, 0, .2);
    margin: 0 auto;
    transition: .3s ease-out all;
    animation: 1s pulse ease-out infinite;
    animation-delay: .3s;
}
.illustrative a.main-cta:hover {
    background: rgb(6, 209, 209);
    transform: scale(1.05);
}
@keyframes pulse {
    0% {
        box-shadow: 3px 3px 30px rgba(0, 0, 0, .2);
    }
    50% {
        box-shadow: 3px 3px 30px rgba(148, 11, 228, 0.4);
    }
}

.separator {
    margin: 50px auto;
    display: table;
}

@media screen and (max-width: 768px) {

    .wrapper .infobox,
    .wrapper .illustrative {
        width: 100% !important;
    }

    .wrapper .infobox img,
    .wrapper .illustrative img {
        width: 100%;
        height: auto;
    }
    .subheading {
        text-align: center;
    }
}

@media screen and (min-width: 1920px) {
    .wrapper {
        justify-content: center;
        align-items: center;
    }
    .wrapper .infobox,
    .wrapper .illustrative {
        width: 100% !important;
        max-width: 500px;
    }

    .wrapper .infobox img,
    .wrapper .illustrative img {
        width: 100%;
        max-width: 400px;
        height: auto;
    }
}
</style>
