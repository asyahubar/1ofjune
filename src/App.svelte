<script>
  import mainImg from './assets/ukraine.jpeg'
  import qr from './assets/form_qr.svg'
  import natureImg from './assets/nature.svg'
  import Footer from './lib/Footer.svelte'
  import TailwindCss from './lib/TailwindCSS.svelte';

  let lang = 'uk'
  let embOnMap = 'https://www.google.com/maps/place/Embassy+of+Ukraine/@44.7727203,20.4594424,17z/data=!3m1!4b1!4m5!3m4!1s0x475a704efbff6dd5:0xbb490a4f707cb2db!8m2!3d44.7727165!4d20.4616311'
  let regForm = 'https://docs.google.com/forms/d/1MoMlMx__uhagZmzeF9nsHnrw5w9i2CmmjUMkiOmZyyw/viewform?edit_requested=true'
</script>
<TailwindCss />

<section class="layout">
  <div class="main-img">
    <img src={mainImg} alt="Долоні обіймають сердечко. Авторка: Agnieszka Srokosz"/>
  </div>
  <main>
    <p class="subtitle">За підтримки Посольства України в Сербії та громади</p>

    <h1>Захід до Дня захисту дітей</h1>

    <div class="announcement text-red-500 p-8 border-dashed border-red-500 border rounded font-medium">Дякуємо усім за ваш інтерес. Реєстрація завершена. Всі зареєстровані отримають запрошення на імейл.</div>

    <!-- <p>
      Чекаємо на вас <strong>1 червня </strong> у Посольстві України в Сербії за адресою <a href={embOnMap}>вул.Пає Адамова 4 у Белграді</a>.
      Точний час зустрічі та програму ви отримаєте після реєстрації.
    </p> -->

    <hr>
    <!-- <h2>Щоб доєднатися, потрібно:</h2>

    <ul class="conditions">
      <li>
        <figure>
          <img src={qr} alt="QR code" class="w-72 p-4">
          <figcaption>Попередньо зареєструватися <a href={regForm}>в Google формі</a></figcaption>
        </figure>
      </li>
      <li>
        <div class="slider">
          <div class="slide">
            <img src={natureImg} alt="Nature illustration" class="w-72 p-4">
          </div>
          <div class="slide">
            <ul>
              <li>моє улюблене місто</li> 
              <li>мої улюблені квіти</li>
              <li>я займаюсь спортом</li>
              <li>отака вона моя Україна</li>
              <li>ось так я бачу Сербію</li>
              <li>улюблена розвага</li>
              <li>миру- мир</li>
              <li>тощо</li>
            </ul>
          </div>
        </div>
        <p>Вхідний квиток, себто малюнок на одну з тем</p>
      </li>
    </ul> -->
  
    <Footer />
  </main>
</section>


<style>
  @font-face {
    font-family: 'e-Ukraine';
    src: url('./assets/fonts/e-Ukraine-Thin.ttf') format('ttf');
    font-weight: 200;
  }
  @font-face {
    font-family: 'e-Ukraine';
    src: url('./assets/fonts/e-Ukraine-Medium.ttf') format('ttf');
    font-weight: 400;
  }
  @font-face {
    font-family: 'e-Ukraine';
    src: url('./assets/fonts/e-Ukraine-Bold.ttf') format('ttf');
    font-weight: 700;
  }

  :root {
    font-family: 'e-Ukraine', 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: 400;
  }

  .layout {
    display: flex;
    flex-direction: column;
    font-size: 1.5rem;
    font-weight: 400;
  }

  main {
    /* text-align: center; */
    padding: 1em;
    max-width: 65em;
    /* margin: 0 auto; */
  }

  .main-img {
    height: 16rem;
    width: 100%;
  }
  .main-img img {
    position: static;
    height: 16rem;
    width: 100%;
    object-fit: cover;
  }

  @media screen and (min-width: 800px) {
    .layout {
      flex-direction: row;
    }

    .main-img {
      height: 100vh;
      min-width: 32vw;
      width: auto;
    }
    .main-img img {
      position: fixed;
      height: 100vh;
      width: 32vw;
    }
  }

  h1 {
    color: #0057b8;
    /* text-transform: uppercase; */
    font-size: 3.25rem;
    font-weight: 700;
    line-height: 1.1;
    margin: 2rem 0;
    /* max-width: 14rem; */
  }

  .subtitle {
    color: grey;
    font-size: 1rem;
    margin-bottom: -1.5rem;
    font-weight: 400;
  }

  p {
    /* max-width: 14rem; */
    margin: 1rem 0;
    line-height: 1.35;
  }

  a {
    color: #0057b8;
  }
  a:hover {
    text-decoration: underline;
  }

  hr {
    border-bottom: 1px dashed #0057b8;
    border-left: 0;
    border-top: 0;
    border-right: 0;
    margin: 1rem 0;
  }

  .conditions {
    display: flex;
    gap: 3ch;
    list-style-type: none;
    margin: 0;
    padding: 0;
  }
  .conditions > li {
    margin: 0;
    padding: 1rem;
    border: 1px solid grey;
    border-radius: 1rem;
    max-width: 25rem;
  }
  /* .conditions > li::before {
    content: '☑';
    width: 5px;
    height: 10px;
    object-fit: contain;
    margin-inline-end: 1ch;
  } */
  .conditions ul {
    list-style-type: disc;
    margin-inline-start: 5ch;
    margin-block-start: .4rem;
    font-size: 1.25rem;
  }
  .conditions ul li {
    padding: .4rem 0;
  }
</style>