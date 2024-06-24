<template>
<header>
    <div class="container">
        <div class="d-flex flex-wrap gap-5 justify-content-center align-items-center">
            <div class="infobox">
                <img src="@/assets/main-image.png" alt="Desvende a Web Com HTML & CSS! EM até 12x de R$ 15,09!">
                <p class="default">Aprenda as linguagens HTML e CSS do zero e crie sites incríveis sem precisar saber programar!</p>
                <h1 class="yellow">Inscreva-se agora e garanta:</h1>
                <ul>
                    <li>
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Desconto especial de lançamento: de R$ 497,00 por apenas R$ 197,00!</span>
                    </li>
                    <li>
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Pagamento facilitado em até 12 parcelas de R$ 15,09.</span>
                    </li>
                    <li>
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Bônus exclusivos, como e-book gratuito e modelos prontos para usar.</span>
                    </li>
                    <li>
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Acesso imediato às aulas e materiais do curso.</span>
                    </li>
                </ul>
            </div>
            <figure>
                <img src="@/assets/ilustrative-image.png" alt="Curso HTML + CSS">
                <a href="#" target="_blank" rel="noopener" class="btn-cta-header">INSCREVA-SE AGORA</a>
            </figure>
        </div>
    </div>
    <img src="@/assets/separator.png" class="separator">
</header>
</template>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');
@import url('https://fonts.cdnfonts.com/css/neo-sans-std');

body {
    background: #141933 !important;
    color: #FFF !important;
    font-family: 'Open Sans', sans-serif !important;
}

header {
    width: 100vw;
    min-height: 100vh;
    background: url('@/assets/header-background.png') no-repeat;
    background-size: cover;
    background-position: center;
    padding-top: 100px;
    position: relative;
}

.infobox {
    display: flex;
    flex-direction: column;
    gap: 15px;
    max-width: 50%;
}

.infobox img {
    width: 100%;
    max-width: 500px;
    height: auto;
}

p.default {
    font-family: 'Open Sans', sans-serif !important;
    font-size: 20px;
    font-weight: 500;
    line-height: 1.6;
}

h1.yellow {
    font-family: 'Neo Sans Std', sans-serif !important;
    color: #FFC32A;
    font-size: 25px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 15px;
}

figure {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 50%
}

figure img {
    max-width: 500px;
    height: auto;
}

.infobox ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.infobox ul li {
    display: flex;
    gap: 7px;
    align-items: center;
    font-size: 18px;
    font-weight: 500;
}

.infobox ul li i {
    color: #26D8FF;
}

figure a.btn-cta-header {
    color: #FFF;
    text-decoration: none;
    font-size: 22px;
    font-weight: 500;
    font-family: 'Open Sans', sans-serif;
    background: #952AFF;
    border-radius: 16px;
    padding: 16px 50px;
    box-shadow: 3px 3px 30px rgba(0, 0, 0, .2);
    transition: .3s ease all;
    position: relative;
    animation: 1s pulse ease-in infinite;
}

@keyframes pulse {
  0% { box-shadow: 3px 3px 30px rgba(0, 0, 0, .2); }
  60% { box-shadow: 3px 3px 30px rgba(230, 38, 255, 0.5); }
  100% { box-shadow: 3px 3px 30px rgba(0, 0, 0, .2); }
}

@keyframes pulseHover {
  0% { box-shadow: 3px 3px 30px rgba(0, 0, 0, .2); }
  60% { box-shadow: 0 0 30px rgba(38, 216, 255, .3); }
  100% { box-shadow: 3px 3px 30px rgba(0, 0, 0, .2); }
}

figure a.btn-cta-header:hover {
    background: #26D8FF;
    box-shadow: 0 0 30px rgba(38, 216, 255, .2);
    transform: scale(1.1);
    animation: 1s pulseHover ease-out infinite;
}

.separator {
    position: absolute;
    bottom: 2vh;
    left: 50%;
    transform: translateX(-50%);
}
</style>
