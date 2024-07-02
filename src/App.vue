<template>
<!-- Starting First Section -->
<header>
    <div class="container">
        <div class="row">
            <div class="col-md-8">
                <img src="@/assets/animated-title.gif" class="main-image">
                <p class="intro" style="padding-left: 30px;">
                    Aprenda as linguagens HTML e CSS do zero e crie sites incríveis sem precisar saber programar!
                </p>
                <h2 class="neo-sans-yellow-title" style="padding-left: 30px;">Inscreva-se agora e garanta:</h2>
                <ul class="items-list" style="padding-left: 30px;">
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
                <img src="@/assets/html-and-css.gif" class="ilustrative">
                <button type="button" class="cta-btn" @click="redirectToPayment">INSCREVA-SE AGORA</button>
            </div>
        </div>
    </div>
</header>
<!-- Ending First Section -->

<img src="@/assets/separator.png" class="separator">

<!-- Starting Second Section -->
<section class="why">
    <div class="container">
        <div class="flex">
            <h2>
                <span class="medium-weight d-block">Por que escolher o curso</span>
                <span class="black-weight">Desvende a Web com HTML &amp; CSS?</span>
            </h2>
            <div class="cards">
                <div class="card-item">
                    <i class="bi bi-star-fill"></i>
                    <p>Curso completo para iniciantes: Aprenda tudo o que precisa saber para dominar HTML e CSS, desde as bases até técnicas avançadas.</p>
                </div>
                <div class="card-item">
                    <i class="bi bi-star-fill"></i>
                    <p>Aulas em vídeo e exercícios práticos: Aprenda em seu próprio ritmo e consolide seu conhecimento com exercícios práticos.</p>
                </div>
                <div class="card-item">
                    <i class="bi bi-star-fill"></i>
                    <p>Suporte dedicado: Tire suas dúvidas e obtenha ajuda sempre que precisar com nossa equipe de suporte.</p>
                </div>
                <div class="card-item">
                    <i class="bi bi-star-fill"></i>
                    <p>Comunidade vibrante: Junte-se à nossa comunidade online de alunos e profissionais de web design para trocar ideias e experiências.</p>
                </div>
                <div class="card-item">
                    <i class="bi bi-star-fill"></i>
                    <p>Acesso vitalício: Tenha acesso ilimitado às aulas e materiais do curso para sempre.</p>
                </div>
                <div class="card-item">
                    <i class="bi bi-star-fill"></i>
                    <p>Certificado de conclusão: Comprovante de suas habilidades recém-adquiridas para impressionar futuros empregadores ou clientes.</p>
                </div>
            </div>
            <button type="button" class="clouds-cta-btn" @click="redirectToPayment">INSCREVA-SE AGORA</button>
        </div>
    </div>
</section>
<!-- /Endind Second Section -->

<!-- Starting FAQ's -->
<section class="faq py-5">
    <div class="container mt-4">
        <h2 class="text-center neo-sans-title">Perguntas frequentes</h2>
        <div class="dropdown-card" v-for="(faq, index) in faqs" :key="faq.id" @click="toggleDropdown(index)">
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
        <img src="@/assets/separator.png" class="mx-auto d-table">
        <h3 class="neo-sans-yellow-section-title">
            Não deixe essa <br />
            oportunidade passar!
        </h3>
        <p class="last-section-text">
            Inscreva-se agora e comece sua jornada como web designer de sucesso!
        </p>
        <button type="button" class="last-section-cta" @click="redirectToPayment">
            INSCREVA-SE AGORA
        </button>
    </div>
</section>
<!-- /Ending Last Section -->

 <!-- Starting Footer Section -->
<footer>
    <div class="container">
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
    font-size: 20px;
    font-family: 'Open Sans', sans-serif;
    font-weight: 600;
    line-height: 1.7;
    margin-top: 40px;
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
    background: url("@/assets/clouds-background.png") no-repeat;
    background-position: center bottom;
}

.flex {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 100px 0;
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

.cards {
    display: flex;
    flex-direction: column;
    gap: 15px;
    margin-top: 40px;
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
    margin-top: 30px;
    box-shadow: 2px 2px 30px rgba(38, 216, 255, .2);
    animation: 1s fadeInClouds ease infinite;
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
</style>
