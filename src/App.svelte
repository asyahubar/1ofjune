<script>
  import mainImg from './assets/ukraine.jpeg'
  import qr from './assets/form_qr.svg'
  import natureImg from './assets/nature.svg'
  import Footer from './lib/Footer.svelte'
  import TailwindCss from './lib/TailwindCSS.svelte';

  let lang = 'uk'
  let embOnMap = 'https://www.google.com/maps/place/Embassy+of+Ukraine/@44.7727203,20.4594424,17z/data=!3m1!4b1!4m5!3m4!1s0x475a704efbff6dd5:0xbb490a4f707cb2db!8m2!3d44.7727165!4d20.4616311'
  let regForm = 'https://docs.google.com/forms/d/1MoMlMx__uhagZmzeF9nsHnrw5w9i2CmmjUMkiOmZyyw/viewform?edit_requested=true'
  const variableFontGuide = 'https://glyphsapp.com/learn/creating-a-variable-font'
  const notoSerifVariable = 'https://fonts.google.com/noto/specimen/Noto+Serif+Display?vfonly=true'
  const variableFontCss = 'https://etceteratype.co/blog/animating-a-variable-font-with-css'

  let wght = 100
</script>
<TailwindCss />

<section class="layout">
  <div class="main-img">
  </div>
  <main>
    <h2 style="--wght: {wght}">
      Here we go
    </h2>
    <p>{wght}</p>
    <input type="range" id="wght" name="wght" min="100" max="900" bind:value={wght}>
    <!-- <h3>
      <span style="--delay: 0.1s">H</span>
      <span style="--delay: 0.2s">e</span>
      <span style="--delay: 0.3s">r</span>
      <span style="--delay: 0.4s">e</span> 
      <span style="--delay: 0.5s">w</span>
      <span style="--delay: 0.6s">e</span> 
      <span style="--delay: 0.7s">g</span>
      <span style="--delay: 0.8s">o</span>
    </h3> -->
    <h3>Loading
      <span style="--delay: 0.1s">.</span>
      <span style="--delay: 0.3s">.</span>
      <span style="--delay: 0.5s">.</span>
    </h3>
    <Footer />
  </main>
</section>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+Display:wght@100..900');
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
  /* @font-face {
    font-family: 'Noto Serif Display', serif;
    src: url('./assets/fonts/NotoSerifDisplay-VariableFont_wdth,wght.ttf') format('ttf') tech('variations');
    font-weight: 100 900;
  } */

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
    width: 100%;
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

  h2 {
    color: #0057b8;
    /* text-transform: uppercase; */
    font-family: 'Noto Serif Display';
    font-size: 3.25rem;
    /* font-weight: 700; */
    font-variation-settings: 'wght' var(--wght);
    line-height: 1.1;
    margin: 2rem 0;
    /* max-width: 14rem; */
  }

  h3 {
    display: block;
    font-family: 'Noto Serif Display';
    font-size: 4rem;
    color: crimson;
    line-height: 1.1;
    margin: 2rem 0;
  }

  h3 span {
    text-transform: capitalize;
    animation: bolden ease 1.1s var(--delay) infinite;
    width: 2em;
  }

  @keyframes bolden {
    from {
      font-variation-settings: 'wght' 900;
    }
    45% {
      font-variation-settings: 'wght' 100;
    }
    55% {
      font-variation-settings: 'wght' 100;
    }
    to {
      font-variation-settings: 'wght' 900;
    }
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