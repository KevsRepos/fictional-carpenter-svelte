<script>
  import ImageCard from "../components/ImageCard.svelte";
  import Formular from "../components/index/Formular.svelte";
  import NumberSlider from "../components/index/NumberSlider.svelte";
  import References from "../components/index/References.svelte";

  const card1 = {
    imgPath: './images/dachstuhl.jpg',
    imgAlt: 'Dachstühle',
    headline: 'Dachstühle',
    description: 'Kerngeschäft sind unsere qualitativ verarbeiteten Dachstühle, welche wir mit Feinarbeit und guter Planung im Voraus aufstellen. In 15 Jahren haben wir bereits über 4000 Dachstühle professionell und makellos aufgestellt.'
  }

  const card2 = {
    imgPath: './images/dachstuhl.jpg',
    imgAlt: 'Dachstühle',
    headline: 'Dachstühle',
    description: 'Kerngeschäft sind unsere qualitativ verarbeiteten Dachstühle, welche wir mit Feinarbeit und guter Planung im Voraus aufstellen. In 15 Jahren haben wir bereits über 4000 Dachstühle professionell und makellos aufgestellt.'
  }

  const card3 = {
    imgPath: './images/dachstuhl.jpg',
    imgAlt: 'Dachstühle',
    headline: 'Dachstühle',
    description: 'Kerngeschäft sind unsere qualitativ verarbeiteten Dachstühle, welche wir mit Feinarbeit und guter Planung im Voraus aufstellen. In 15 Jahren haben wir bereits über 4000 Dachstühle professionell und makellos aufgestellt.'
  }

  const card4 = {
    imgPath: './images/dachstuhl.jpg',
    imgAlt: 'Dachstühle',
    headline: 'Dachstühle',
    description: 'Kerngeschäft sind unsere qualitativ verarbeiteten Dachstühle, welche wir mit Feinarbeit und guter Planung im Voraus aufstellen. In 15 Jahren haben wir bereits über 4000 Dachstühle professionell und makellos aufgestellt.'
  }
</script>

<style>
  .frontBanner {
    height: 90vh;
  }
  .frontBanner:before {
    content: "";
    position: absolute;
    top: 0px;
    left: 0px;
    z-index: -1;
    opacity: 0.8;
    height: 90vh;
    width: 100vw;
    background-image: url('/./images/bannerPic.jpg');
    background-size: cover;
  }
  .c2aCard {
    position: relative;
    top: 25vh;
    left: 15px;
    padding: 15px;
    background-color: var(--transparentWhite);
    display: inline-block;
    width: 500px;
    border-radius: var(--mainRadius);
    opacity: 1;
  }
  .c2aCard p {
    margin: 10px 0;
  }
  .arrowDown {
    position: absolute;
    top: 80vh;
    left: 50%;
    transform: translateX(-50%);
  }
  .imageCards {
    display: flex;
    justify-content: center;
    flex-direction: row;
    flex-wrap: wrap;
    overflow-x: auto;
    margin-left: 30px;
    margin-right: 30px;
  }

  @media screen and (max-width: 650px) {
	.c2aCard {
		width: 90vw;
    left: 50%;
    transform: translateX(-50%);
	}
}
</style>
  
<div class="frontBanner">
  <div class="c2aCard">
    <h1 class="uppercase brandingColor">Mit viel Leidenschaft dabei</h1>
    <p>
      Wir bauen Ihre Dachstühle, Holzverkleidungen,
      Gartenhütten, Schuppen, Scheunen und alles,
      was Ihr Herz begehrt.
    </p>
    <a class="c2a" href="#Anfragen">Fragen Sie uns jetzt an!</a>
  </div>
</div>
<svg class="arrowDown" xmlns="http://www.w3.org/2000/svg" width="29.25" height="29.25" viewBox="0 0 29.25 29.25">
  <g id="Icon_ionic-ios-arrow-dropdown" data-name="Icon ionic-ios-arrow-dropdown" transform="translate(-3.375 -3.375)">
    <path id="Pfad_1" data-name="Pfad 1" d="M10.378,14.815a1.362,1.362,0,0,0,0,1.92l6.729,6.708a1.356,1.356,0,0,0,1.87.042l6.63-6.609a1.355,1.355,0,1,0-1.912-1.92L18,20.566l-5.7-5.759A1.356,1.356,0,0,0,10.378,14.815Z" fill="#fff"/>
    <path id="Pfad_2" data-name="Pfad 2" d="M3.375,18A14.625,14.625,0,1,0,18,3.375,14.623,14.623,0,0,0,3.375,18ZM26.747,9.253A12.37,12.37,0,1,1,9.253,26.747,12.37,12.37,0,1,1,26.747,9.253Z" fill="#fff"/>
  </g>
</svg>

<h1 class="middle uppercase">Was wir leisten</h1>

<section class="imageCards">
  <ImageCard {...card1} />
  <ImageCard {...card2} />
  <ImageCard {...card3} />
  <ImageCard {...card4} />
</section>

<h1 class="middle uppercase">Referenzen</h1>

<References />

<h1 class="middle uppercase">Zahlen die Überzeugen</h1>

<NumberSlider />

<h1 class="middle uppercase">Fragen?</h1>

<Formular />