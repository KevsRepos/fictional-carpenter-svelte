<script>
  export let imgPath, imgAlt, headline, description;
</script>

<style>
  .imgCard {
    border-radius: var(--mainRadius);
    box-shadow: var(--mainBoxShadow);
    position: relative;
    width: min-content;
    padding-bottom: 15px;
    background-color: #ffffff;
    margin: 30px;
  }
  img {
    width: 300px;
    border-top-left-radius: var(--mainRadius);
    border-top-right-radius: var(--mainRadius);
  }
  .headline {
    padding: 10px;
    border-radius: var(--mainRadius);
    background-color: var(--transparentWhite);
    box-shadow: var(--mainBoxShadow);
    position: absolute;
    top: 25%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 999;
    color: var(--brandingColor);
    font-family: 'Caladea', serif;
  }
  .description {
    padding: 20px;
  }
  .c2a {
    word-spacing: 10px;
  }
</style>

<div class="imgCard">
  <img alt={imgAlt} src={imgPath} />
  <span class="headline uppercase">{headline}</span>
    <div class="description">
      {description}
    </div>
    <a class="c2a" href="#anfragen">
      Anfragen 🡢
    </a>
</div>
