<template>
<!-- Starting First Section -->
<header>
    <div class="container">
        <div class="row">
            <div class="col-md-8">
                <!-- Starting Animated Title -->
                <div class="wrapper">
                    <img src="@/assets/tag.png" class="tag">
                    <div class="text-content">
                        <h1 class="headline-1">Desvende a Web</h1>
                        <h2 class="headline-2">Com HTML &amp; CSS!</h2>
                        <h3 class="headline-3">Em até 12x de R$15,09</h3>
                    </div>
                </div>
                <!-- Ending Animated Title -->
                <p class="intro">
                    Aprenda as linguagens HTML e CSS do zero e crie sites incríveis sem precisar saber programar!
                </p>
                <h2 class="neo-sans-yellow-title appear">Inscreva-se agora e garanta:</h2>
                <ul class="items-list">
                    <li class="item">
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Desconto especial de lançamento: de R$ 497,00 por apenas R$ 197,00!</span>
                    </li>
                    <li class="item">
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Pagamento facilitado em até 12 parcelas de R$ 15,09.</span>
                    </li>
                    <li class="item">
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Bônus exclusivos, como e-book gratuito e modelos prontos para usar.</span>
                    </li>
                    <li class="item">
                        <i class="bi bi-check-circle-fill"></i>
                        <span>Acesso imediato às aulas e materiais do curso.</span>
                    </li>
                </ul>
            </div>
            <div class="col-md-4">
                <div class="wrapper-html-and-css">
                    <div class="shape-background">
                        <img src="@/assets/waves-outline.png" class="waves-outline">
                        <img src="@/assets/waves-fill.png" class="waves-fill">
                        <img src="@/assets/html5.png" class="html5">
                        <img src="@/assets/css3.png" class="css3">
                        <img src="@/assets/sparkle.png" class="sparkle-1">
                        <img src="@/assets/sparkle.png" class="sparkle-2">
                    </div>
                </div>
                <button type="button" class="cta-btn" @click="redirectToPayment">INSCREVA-SE AGORA</button>
            </div>
        </div>
    </div>
</header>
<!-- Ending First Section -->

<img src="@/assets/separator.png" class="separator appear">

<!-- Starting Second Section -->
<section class="why">
    <div class="left-clouds">
        <img src="@/assets/left-clouds/back-cloud.png" class="cloud-back popUp">
        <img src="@/assets/left-clouds/front-cloud.png" class="cloud-front popUp">
    </div>
    <div class="container py-5">
        <div class="flex d-flex flex-column gap-2 align-items-center">
            <h2>
                <span class="medium-weight d-block appear">Por que escolher o curso</span>
                <span class="black-weight appear">Desvende a Web com HTML &amp; CSS?</span>
            </h2>
            <div class="cards-content">
                <div class="card-item appear">
                    <i class="bi bi-star-fill"></i>
                    <p>Curso completo para iniciantes: Aprenda tudo o que precisa saber para dominar HTML e CSS, desde as bases até técnicas avançadas.</p>
                </div>
                <div class="card-item appear">
                    <i class="bi bi-star-fill"></i>
                    <p>Aulas em vídeo e exercícios práticos: Aprenda em seu próprio ritmo e consolide seu conhecimento com exercícios práticos.</p>
                </div>
                <div class="card-item appear">
                    <i class="bi bi-star-fill"></i>
                    <p>Suporte dedicado: Tire suas dúvidas e obtenha ajuda sempre que precisar com nossa equipe de suporte.</p>
                </div>
                <div class="card-item appear">
                    <i class="bi bi-star-fill"></i>
                    <p>Comunidade vibrante: Junte-se à nossa comunidade online de alunos e profissionais de web design para trocar ideias e experiências.</p>
                </div>
                <div class="card-item appear">
                    <i class="bi bi-star-fill"></i>
                    <p>Acesso vitalício: Tenha acesso ilimitado às aulas e materiais do curso para sempre.</p>
                </div>
                <div class="card-item appear">
                    <i class="bi bi-star-fill"></i>
                    <p>Certificado de conclusão: Comprovante de suas habilidades recém-adquiridas para impressionar futuros empregadores ou clientes.</p>
                </div>
            </div>
            <button type="button" class="clouds-cta-btn appear" @click="redirectToPayment">INSCREVA-SE AGORA</button>
        </div>
    </div>
    <div class="right-clouds">
        <img src="@/assets/right-clouds/back-cloud.png" class="cloud-back popUp">
        <img src="@/assets/right-clouds/front-cloud.png" class="cloud-front popUp">
    </div>
</section>
<!-- /Endind Second Section -->

<!-- Starting FAQ's -->
<section class="faq py-5">
    <div class="container mt-4">
        <h2 class="text-center neo-sans-title appear">Perguntas frequentes</h2>
        <div class="dropdown-card appear" v-for="(faq, index) in faqs" :key="faq.id" @click="toggleDropdown(index)">
            <i class="bi bi-chevron-down" :class="{ 'bi-chevron-up': faq.isActived }"></i>
            <div class="content">
                <p class="info-title">{{ faq.question }}</p>
                <p class="info-text" v-if="faq.isActived">{{ faq.answer }}</p>
            </div>
        </div>
    </div>
</section>
<!-- /Ending FAQ's sesction -->

<!-- Starting Last Section -->
<section class="last-section">
    <div class="container">
        <img src="@/assets/separator.png" class="mx-auto d-table appear">
        <h3 class="neo-sans-yellow-section-title appear">
            Não deixe essa <br />
            oportunidade passar!
        </h3>
        <p class="last-section-text appear">
            Inscreva-se agora e comece sua jornada como web designer de sucesso!
        </p>
        <button type="button" class="last-section-cta appear" @click="redirectToPayment">
            INSCREVA-SE AGORA
        </button>
    </div>
</section>
<!-- /Ending Last Section -->

 <!-- Starting Footer Section -->
<footer>
    <div class="container appear">
        <div class="footer">
            <div class="company-info">
                <a href="https://www.woxiee.vercel.app" target="_blank" rel="noopener">
                    <img src="@/assets/logo.png" alt="Woxiee">
                </a>
                <a href="mailto:suporte@woxiee.com" target="_blank" rel="noopener" class="emailaddress">suporte@woxiee.com</a>
                <span class="cnpj">41.562.138/0001-61</span>
            </div>
            <div class="social-media">
                <h3>Acompanhe</h3>
                <div class="social-items">
                    <a href="#" target="_blank" rel="noopener" class="social-link">
                        <i class="bi bi-instagram"></i>
                    </a>
                    <a href="#" target="_blank" rel="noopener" class="social-link">
                        <i class="bi bi-facebook"></i>
                    </a>
                    <a href="#" target="_blank" rel="noopener" class="social-link">
                        <i class="bi bi-twitter-x"></i>
                    </a>
                </div>
            </div>
        </div>
    </div>
</footer>
 <!-- /Ending Footer Section -->
</template>

<script>
export default {
  data () {
    return {
      faqs: [{
        id: 1,
        question: 'Qual o valor do curso?',
        answer: 'O valor original do curso é de R$ 497,00. Mas por tempo limitado, você pode adquirir o curso por apenas R$ 197,00 com pagamento facilitado em até 12x de R$ 15,09.',
        isActived: true
      },
      {
        id: 2,
        question: 'Como posso me inscrever no curso?',
        answer: "Para se inscrever no curso, basta clicar no botão 'Inscrever-se' na página do curso. Em seguida, você será direcionado para a página de pagamento, onde poderá escolher a forma de pagamento que preferir.",
        isActived: false
      },
      {
        id: 3,
        question: 'Como posso realizar o pagamento?',
        answer: 'Você pode realizar o pagamento do curso com cartão de crédito, boleto bancário ou Pix. O pagamento é processado de forma segura pela Hotmart.'
      },
      {
        id: 4,
        question: 'Qual o prazo de acesso ao curso?',
        answer: 'Você terá acesso ao curso por 1 ano após a data da compra. Durante esse período, você poderá assistir às aulas quantas vezes quiser, baixar os materiais do curso e tirar suas dúvidas com os professores.'
      },
      {
        id: 5,
        question: 'Tenho garantia de satisfação?',
        answer: 'Sim, oferecemos uma garantia de satisfação de 7 dias. Se você não estiver satisfeito com o curso, poderá solicitar o reembolso integral do seu dinheiro.'
      }
      ]
    }
  },
  methods: {
    toggleDropdown (index) {
      this.faqs.forEach((faq) => (faq.isActived = false))
      this.faqs[index].isActived = !this.faqs[index].isActived
    },
    redirectToPayment () {
      window.location.href = 'https://pay.hotmart.com/T93819108Q'
    }
  }
}
</script>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');
@import url('https://fonts.cdnfonts.com/css/neo-sans-std');

body {
    background: #141933 !important;
    color: #FFF !important;
    font-family: 'Open Sans', sans-serif !important;
}

::-webkit-scrollbar {
    width: 3px;
    height: 3px;
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
header {
    min-height: 100vh;
    display: flex;
    align-items: center;
}

@media screen and (max-width: 700px) {
    header {
        padding-top: 50px;
    }
}

.main-image {
    width: 100%;
    height: auto;
    max-width: 600px;
}

p.intro {
    font-size: 1.2rem;
    font-family: 'Open Sans', sans-serif;
    font-weight: 500;
    line-height: 1.7;
    margin-top: 3rem;
}

.ilustrative {
    width: 100%;
    height: auto;
    margin-top: 100px;
}

@media screen and (max-width: 700px) {
    .ilustrative {
        margin-top: -10px;
    }
}

/*
    Second Section "Why"
*/
.why {
    width: 100%;
    min-height: 100vh;
    display: table;
    background-image: linear-gradient(to bottom, #141933, #232a4e);
    position: relative;
}

.flex h2 {
    text-align: center;
    font-family: 'Neo Sans Std', sans-serif;
    text-transform: uppercase;
    font-size: 35px;
    line-height: 1.4;
}

.medium-weight {
    font-weight: 400;
}

.black-weight {
    font-weight: 700;
}

h2.neo-sans-yellow-title {
    font-size: 25px;
    font-weight: 600;
    letter-spacing: 1px;
    font-family: 'Neo Sans Std', sans-serif;
    line-height: 1.5;
    color: #FFC32A;
    text-transform: uppercase;
}

.items-list {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 15px;
}

li.item {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    font-size: 18px;
    font-family: 'Open Sans', sans-serif;
    color: #FFF;
    line-height: 1.5;
    font-weight: 500;
}

li.item i {
    color: #26D8FF;
}

.cta-btn {
    text-decoration: none;
    color: #FFF;
    font-family: 'Open Sans', sans-serif;
    font-size: 19px;
    font-weight: 500;
    padding: 12px 50px;
    display: table;
    margin: 0 auto;
    border-radius: 15px;
    background: #952AFF;
    border: none;
    box-shadow: 2px 2px 30px rgba(172, 9, 248, 0.3);
    animation: 1s fadeIn ease infinite;
}

@keyframes fadeIn {

    0%,
    100% {
        box-shadow: 2px 2px 30px rgba(172, 9, 248, 0.3);
    }

    50% {
        box-shadow: 2px 2px 50px rgba(172, 9, 248, 0.5);
    }
}

.separator {
    margin: 0 auto;
    display: table;
}

@media screen and (max-width: 700px) {
    .cta-btn {
        margin-bottom: 100px;
    }
}

.cards-content {
    display: flex;
    flex-direction: column;
    row-gap: 15px;
    margin-top: 40px;
    transition: .3s ease all;
}

.card-item {
    background: #952AFF;
    padding: 20px 30px;
    border-radius: 20px;
    display: flex;
    gap: 10px;
    align-items: center;
    box-shadow: 2px 2px 30px rgba(0, 0, 0, .2);
}

.card-item p {
    font-size: 18px;
    font-weight: 500;
    font-family: 'Open Sans', sans-serif;
    color: #FFF;
    margin: 0;
    line-height: 1.4;
}

.card-item i {
    color: #FFC32A;
}

.clouds-cta-btn {
    border: none;
    background: #2AB2FF;
    border-radius: 15px;
    font-size: 19px;
    font-weight: 500;
    font-family: 'Open Sans', sans-serif;
    padding: 13px 40px;
    color: #FFF;
    display: table;
    margin: 30px auto;
    box-shadow: 2px 2px 30px rgba(38, 216, 255, .2);
    animation: 1s fadeInClouds ease infinite;
    cursor: pointer !important;
}

@keyframes fadeInClouds {

    0%,
    100% {
        box-shadow: 2px 2px 30px rgba(38, 216, 255, .2);
    }

    50% {
        box-shadow: 2px 2px 30px rgba(38, 216, 255, .5);
    }
}

.faq {
    background: #952AFF;
    width: 100%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
}

section.faq::before {
    content: '';
    position: absolute;
    top: -40px;
    left: 0;
    width: 100%;
    height: 100px;
    background: #952AFF;
    transform: skewY(-2deg);
    z-index: 0;
}

.neo-sans-title {
    font-size: 30px;
    letter-spacing: 1px;
    color: #FFF;
    font-weight: 500;
    font-family: 'Neo Sans Std', sans-serif;
    line-height: 1.5;
    margin: 0 0 40px 0;
    text-transform: uppercase;
}

.dropdown-card {
    display: inline-flex;
    width: 100%;
    margin-bottom: 15px;
    gap: 10px;
    align-items: baseline;
    padding: 20px;
    border-radius: 15px;
    background: #AA5FF4;
    box-shadow: 2px 2px 30px rgba(0, 0, 0, .1);
    transition: .3s ease all;
    cursor: pointer;
}

p.info-title {
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    font-weight: 700;
    line-height: 1.5;
    margin: 0;
}

p.info-text {
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.5;
    margin: 5px 0 0 0;
}

  .dropdown-card:hover {
    background-color: #ba7afa;
  }

  .dropdown-card i {
    margin-right: 15px;
    transition: transform 0.3s ease;
  }

  .dropdown-card.bi-chevron-up i {
    transform: rotate(180deg);
  }

  .content {
    flex: 1;
  }

  .info-title {
    font-weight: bold;
    margin-bottom: 5px;
  }

  .last-section {
    width: 100%;
    min-height: 100vh;
    background: url('@/assets/arrows-background.png') no-repeat;
    background-size: cover;
    background-position: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .neo-sans-yellow-section-title {
    font-family: 'Neo Sans Std', sans-serif;
    font-size: 40px;
    font-weight: 600;
    color: #FFC32A;
    text-transform: uppercase;
    letter-spacing: 1px;
    line-height: 1.3;
    margin: 30px 0 0 0;
    text-align: center;
  }

  .last-section-text {
    font-size: 25px;
    font-weight: 600;
    font-family: 'Open Sans', sans-serif;
    text-align: center;
    margin: 15px 0 0 0;
    line-height: 1.5;
  }

  .last-section-cta {
    color: #FFF;
    font-family: 'Open Sans', sans-serif;
    font-size: 22px;
    font-weight: 600;
    padding: 14px 30px;
    display: table;
    background: #952AFF;
    border: 1px solid #CD8DFF;
    box-shadow: 2px 2px 30px rgba(149, 42, 255, .5);
    border-radius: 15px;
    margin: 30px auto;
    animation: 1s pulse ease infinite;
  }

  @keyframes pulse {
    0%, 100% { transform: scale(1); box-shadow: 2px 2px 30px rgba(149, 42, 255, .2); }
    50% { transform: scale(1.05); box-shadow: 2px 2px 30px rgba(149, 42, 255, .5); }
  }

  footer {
    width: 100%;
    padding: 30px 0;
    background: #080B1D;
  }
  .footer {
    display: flex;
    width: 100%;
    justify-content: space-between;
  }
  .company-info {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .emailaddress {
    font-size: 18px;
    font-weight: 500;
    font-family: 'Open Sans', sans-serif;
    line-height: 1.5;
    color: #28C6E9;
    text-decoration: none;
    margin-top: 10px;
  }
  .cnpj {
    font-size: 18px;
    font-weight: 500;
    font-family: 'Open Sans', sans-serif;
    line-height: 1.5;
    color: #6872AF;
  }

  .social-media h3 {
    font-size: 25px;
    color: #FFF;
    font-family: 'Neo Sans Std', sans-serif;
    line-height: 1.5;
    font-weight: 500;
  }
  .social-link {
    color: #26D8FF;
    font-size: 22px;
  }

  .social-items {
    display: flex;
    justify-content: flex-end;
    gap: 20px;
  }

  @media screen and (max-width: 700px) {
    .footer {
        flex-direction: column;
        align-items: center;
    }
    .social-items {
        display: flex;
        justify-content: center;
        gap: 20px;
    }
  }

/*
    Starting Animated Header Title
*/
.wrapper {
    width: 100%;
    max-width: 600px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    position: relative;
    margin-top: 4rem;
}

@media screen and (max-width: 700px) {
    .wrapper {
        margin-top: 50px !important;
        width: 100%;
    }
    .headline-3 {
        font-size: 1.2rem !important;
    }
}

.tag {
    position: absolute;
    z-index: -1;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    opacity: 0;
    animation: 1s bounceIn ease forwards;
    animation-delay: .4s;
}

@media screen and (max-width: 700px) {
    .tag {
        width: 100%;
        height: auto;
        max-width: 550px;
    }
}

.text-content {
    display: table;
    width: 100%;
    position: relative;
}

h1.headline-1 {
    color: #FFF;
    font-size: 2rem;
    font-family: 'Neo Sans Std', sans-serif;
    letter-spacing: 1px;
    text-shadow: 2px 2px 0 #420e75;
    font-weight: 700;
    text-transform: uppercase;
    margin: 0 auto;
    padding: 10px 35px;
    background: #FFC32B;
    border-radius: 10px;
    display: table;
    line-height: 1.2;
    text-align: center;
    box-shadow: 2px 0 30px rgba(0, 0, 0, .2);
    position: relative;
    opacity: 0;
    transform: skew(-9deg) rotate(-5deg);
    z-index: 2;
    animation: 1s swipeInTop ease forwards;
    animation-delay: 1s;
}

h2.headline-2 {
    color: #FFF;
    font-size: 1.8rem;
    font-family: 'Neo Sans Std', sans-serif;
    letter-spacing: 1px;
    text-shadow: 1.5px 1.5px 0 #ac0a89;
    font-weight: 700;
    text-transform: uppercase;
    margin: 0 auto;
    padding: 10px 35px;
    background: #952BFF;
    border-radius: 10px;
    display: table;
    line-height: 1.2;
    text-align: center;
    box-shadow: 2px 0 30px rgba(0, 0, 0, .2);
    position: relative;
    transform: translateY(-8px) skew(-9deg) rotate(-5deg);
    opacity: 0;
    animation: 1s swipeInTop2 ease forwards;
    animation-delay: 1.1s;
    z-index: 3;
}

h3.headline-3 {
    color: #FFF;
    font-size: 1.8rem;
    font-family: 'Neo Sans Std', sans-serif;
    letter-spacing: 1px;
    text-shadow: 1.5px 1.5px 0 #086c83;
    font-weight: 500;
    text-transform: uppercase;
    margin: 0 auto;
    padding: 20px 35px;
    background: #26D8FF;
    border-radius: 900px;
    display: table;
    line-height: 1.2;
    text-align: center;
    box-shadow: 2px 0 30px rgba(0, 0, 0, .2);
    position: relative;
    z-index: 100 !important;
    opacity: 0;
    transform: translateY(-12px) skew(-9deg) rotate(-5deg);
    animation: 1s swipeInTop3 ease forwards;
    animation-delay: 1.2s;
}

h3.headline-3::before {
    content: '';
    position: absolute;
    z-index: -1;
    width: calc(100% + 9px);
    height: calc(100% + 9px);
    border-radius: 900px;
    border: 1.4px solid #55e0ff;
    box-shadow: 0 0 15px rgba(85, 224, 255, .4);
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    animation: 1s neon linear infinite;
}

@keyframes swipeInTop {
    from { transform: translateY(10px) skew(-9deg) rotate(-5deg); opacity: .3; }
    to { transform: translateY(0) skew(-9deg) rotate(-5deg); opacity: 1; }
}

@keyframes swipeInTop2 {
    from { transform: translateY(5px) skew(-9deg) rotate(-5deg); opacity: .3; }
    to { transform: translateY(-8px) skew(-9deg) rotate(-5deg); opacity: 1; }
}

@keyframes swipeInTop3 {
    from { transform: translateY(12px) skew(-9deg) rotate(-5deg); opacity: .3; }
    to { transform: translateY(-12px) skew(-9deg) rotate(-5deg); opacity: 1; }
}

@keyframes neon {
    0% { opacity: 0; }
    3%, 12% { opacity: 1; }
    13% { opacity: 0; }
    14% { opacity: 1; }
    15% { opacity: 0; }
    16% { opacity: 1; }
    17%, 25% { opacity: 0; }
    26%, 45% { opacity: 1; }
    46% { opacity: 0; }
    47% { opacity: 1; }
    48% { opacity: 0; }
    49%, 66% { opacity: 1; }
    67%, 75% { opacity: 0; }
    76% { opacity: 1; }
    77% { opacity: 0; }
    78%, 90% { opacity: 1; }
    91%, 96% { opacity: 0; }
    97%, 100% { opacity: 1; }
}
/*
    Ending Animated Header Title
*/

/*
    Starting HTML & CSS Icons Animated
*/
.wrapper-html-and-css {
    width: 100%;
    max-width: 600px;
    min-height: 600px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    border-radius: 25px;
    position: relative;
}

.shape-background {
    width: 100%;
    max-width: 350px;
    height: 480px;
    background: #303969;
    border-radius: 25px;
    box-shadow: 3px 3px 30px rgba(0, 0, 0, .2);
    display: table;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    transition: .3s ease all;
    animation: 3s bounceIn ease infinite;
    z-index: 10 !important;
}

.shape-background::before {
    content: '';
    width: calc(100% + 14px);
    height: calc(100% + 16px);
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    border: .4px solid #952AFF;
    border-radius: 25px;
    animation: 1.5s pulse ease infinite;
    z-index: -2 !important;
}

.shape-background::after {
    content: '';
    width: calc(100% + 8px);
    height: calc(100% + 8px);
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    border: .4px solid #952AFF;
    border-radius: 25px;
    animation: 1.5s pulse ease infinite;
    animation-delay: .4s;
    z-index: -2 !important;
}

.shape-background img {
    position: absolute;
}

.shape-background img.waves-outline, .shape-background img.waves-fill {
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    width: 85%;
    height: auto;
    animation: 1s rotation ease infinite;
}

.shape-background img.waves-fill {
    animation-delay: .4s;
}

.html5 {
    bottom: -4rem;
    right: -3rem;
    transform: rotate(15deg) scale(.9);
    animation: 3s htmlBalance ease infinite;
}

.css3 {
    top: -5rem;
    left: -5rem;
    transform: rotate(-18deg) scale(1);
    animation: 3s cssBalanceMobile ease infinite;
    animation-delay: .4s;
}

@media screen and (max-width: 600px) {
    .wrapper-html-and-css {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        margin: 2rem auto;
    }
    .html5 {
        bottom: -5rem;
        right: -2.5rem;
        transform: rotate(15deg) scale(.7);
        animation: 3s htmlBalanceMobile ease infinite;
    }

    .css3 {
        top: -2.5rem;
        left: -2rem;
        transform: rotate(-18deg) scale(.8);
    }
}

@keyframes bounceIn {
    0%, 100% { transform: skew(4deg, 2deg) rotate(3deg) scale(1) translate(-50%, -50%); }
    50% { transform: skew(0deg, 0deg) rotate(0deg) scale(1.03) translate(-50%, -50%); }
}

@keyframes htmlBalance {
    0%, 100% { transform: rotate(15deg) scale(.9) translateY(0);  }
    50% { transform: scale(.9) translateY(-2rem) translateX(-.2rem) rotate(-3deg); }
}
@keyframes htmlBalanceMobile {
    0%, 100% { transform: rotate(15deg) scale(.7) translateY(0); }
    50% { transform: scale(.8) translateY(-1rem) translateX(-.5rem) rotate(-1deg); }
}

@keyframes cssBalance {
    0%, 100% { transform: rotate(15deg) scale(.9) translateY(0);  }
    50% { transform: rotate(15deg) scale(.9) translateY(-2rem) translateX(-.5rem) rotate(-3deg); }
}
@keyframes cssBalanceMobile {
    0%, 100% { transform: rotate(-18deg) scale(.9) translateY(0); }
    50% { transform: rotate(-18deg) scale(.9) translateY(-2rem) translateX(-.5rem) rotate(1deg); }
}

@keyframes rotation {
    0%, 100% { transform: scale(1) translate(-50%, -50%); }
    50% { transform: scale(1.03) translate(-50%, -50%); }
}

@keyframes pulse {
    0% { opacity: 0; transform: translate(-50%, -50%) scale(.5); }
    50% { opacity: 1; transform: translate(-50%, -50%) scale(1.02); }
    70% { opacity: .5; transform: translate(-50%, -50%) scale(1.05); }
    100% { opacity: 0; transform: translate(-50%, -50%) scale(1.08); }
}
/*
    Ending HTML & CSS Icons Animated
*/

/*
    Starting Scroll Animation
*/
.appear {
    animation: appear linear;
    animation-timeline: view();
    animation-range: entry 0% cover 40%;
}
@keyframes appear {
    from {
        opacity: 0;
        transform: translateX(-100px);
    }
    to {
        opacity: 1;
        transform: translateX(0px);
    }
}

.popUp {
    animation: popUp linear;
    animation-timeline: view();
    animation-range: entry 0% cover 40%;
}
@keyframes popUp {
    0% {
        opacity: 0;
        transform: scale(0);
    }
    80% {
        opacity: 1;
        transform: scale(1.05);
    }
    90% {
        opacity: 1;
        transform: scale(.9);
    }
    100% {
        opacity: 1;
        transform: scale(1);
    }
}
/*
    Ending Scroll Animation
*/

.left-clouds {
    width: 100%;
    display: table;
    position: absolute;
    bottom: 0;
    overflow: hidden;
}
.left-clouds img.cloud-back {
    position: absolute;
    left: -12rem;
    bottom: -10rem;
}
.left-clouds img.cloud-front {
    position: absolute;
    left: -12rem;
    bottom: -10rem;
}

.right-clouds {
    width: 100%;
    display: table;
    position: absolute;
    bottom: 0;
    overflow: hidden;
}
.right-clouds img.cloud-back {
    position: absolute;
    right: -12rem;
    bottom: -10rem;
}
.right-clouds img.cloud-front {
    position: absolute;
    right: -12rem;
    bottom: -10rem;
}

/*
    Sparkles Starts
*/
.sparkle-1 {
    width: 30px;
    height: auto;
    position: absolute;
    bottom: 0;
    left: 0;
    transform: translateX(0rem) translateY(0rem) scale(1) rotate(0);
    animation: 3.5s sparkle-1 ease infinite;
    animation-delay: .3s;
}

.sparkle-2 {
    width: 15px;
    height: auto;
    position: absolute;
    top: 0;
    right: 0;
    transform: translate(0rem, 0rem) scale(1) rotate(10deg);
    animation: 3.5s sparkle-2 ease infinite;
    animation-delay: .3s;
}

@keyframes sparkle-1 {
    0%, 100% { transform: translateX(0rem) translateY(0rem) scale(.8) rotate(0); }
    50% { transform: translateX(-2rem) translateY(2rem) scale(1) rotate(25deg); }
}

@keyframes sparkle-2 {
    0%, 100% { transform: translate(0rem, 0rem) scale(1) rotate(10deg); }
    50% { transform: translate(2rem, -2rem) scale(1) rotate(15deg); }
}
/*
    Sparkles Ends
*/
</style>
