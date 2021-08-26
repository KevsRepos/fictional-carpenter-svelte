<script>
  const referenceImages = [
    {
      imgPath: 'reference1',
      alt: 'Beispiel',
    },
    {
      imgPath: 'reference2',
      alt: 'Beispiel',
    },
    {
      imgPath: 'reference3',
      alt: 'Beispiel',
    },
    {
      imgPath: 'reference4',
      alt: 'Beispiel',
    },
    {
      imgPath: 'reference5',
      alt: 'Beispiel',
    },
    {
      imgPath: 'reference6',
      alt: 'Beispiel',
    }
  ];
</script>
<style>
  h3, h3 *{
    letter-spacing: 8px;
    color: var(--brandingColor);
  }
  .references {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    border-top: 1px var(--brandingColor) solid;
    border-bottom: 1px var(--brandingColor) solid;
    transform: rotate(-6deg);
    width: 90vw;
    margin: auto;
  }
  .referenceImages {
    width: 9.5vw;
    height: auto;
    margin: 80px 20px;
    transform: rotate(6deg);
    border-radius: var(--mainRadius);
    box-shadow: var(--mainBoxShadow);
    transition: 0.10s ease-in;
  }
  .referenceImages:hover {
    margin-top: 60px;
  }

  @media screen and (max-width: 730px) {
    .references {
      width: 90vw;
    }
    .referenceImages {
      margin: 20px;
      width: 18vw;
    }
  }
</style>

<h3 class="middle">Von den ganz kleinen, zu den ganz <span class="uppercase">Grossen</span></h3>

<div class="references">
  {#each referenceImages as {imgPath, alt}}
    <a href="#referImg"><img class="referenceImages" {alt} src={"../../images/referenceImages/" + imgPath + ".jpg"} /></a>
  {/each}
</div>