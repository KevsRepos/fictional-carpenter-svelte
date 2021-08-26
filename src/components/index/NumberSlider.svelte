<script>
  const numberCircles = [
    ['Mehr als', 50, 'Mitarbeiter'],
    ['Seit fast', 20, 'Jahren am bestehen'],
    ['Über', 700, 'qm Betriebsfläche'],
    ['Über', 300, 'Aufträge im Jahr'],
    ['Mittlerweile', '13.000', 'Kunden, die uns vertrauen']
  ];
</script>

<style>
  * {
    font-family: 'Caladea', serif;
  }
  .numberSlider {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 80vw;
    margin: auto;
  }
  .circle {
    display: flex;
    flex-direction: column;
    padding: 20px;
    box-shadow: var(--mainBoxShadow);
    border-radius: 50%;
    height: 15vw;
    width: 15vw;
    justify-content: center;
    text-align: center;
    margin: 20px 60px;
    border: 2px var(--brandingColor) solid;
    background-color: #ffffff;
  }
  p {
    font-size: clamp(1em, calc(1rem + ((1vw - 0.48em) * 0)), 1em);
  }
  .number {
    font-size: clamp(2.1em, calc(2.1rem + ((1vw - 0.48em) * 2.9167)), 4.2em);
    min-height: 0vw;
  }

  @media screen and (max-width: 655px) {
    .circle {
      margin: 20px;
      height: 50vw;
      width: 50vw;
    }
  }
</style>

<div class="numberSlider">
  {#each numberCircles as [upperText, number, lowerText]}
    <div class="circle">
      <p>{upperText}</p>
      <span class="number">{number}</span>
      <p>{lowerText}</p>
    </div>
  {/each}
</div>