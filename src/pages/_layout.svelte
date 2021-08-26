<script>
  let openMenu = false;
  let firstTouch;

  const touchStart = e => {
    firstTouch = e.touches[0].clientY;
  }

  const touchMove = e => { 
    if(firstTouch <  e.touches[0].clientY - 100) {
      openMenu = false;
    }
  }

  const links = [
    ["#Produkte", "Produkte"],
    ["#Leistungen", "Leistungen"],
    ["#Unternehmen", "Unternehmen"],
    ["#Kontakt", "Kontakt"],
  ]
</script>

<style>
  header {
    padding: 25px;
    display: flex;
    flex-direction: row;
    align-items: center;
    text-transform: uppercase;
    position: fixed;
    width: 100vw;
    background-color: var(--transparentWhite);
    z-index: 9999999;
    box-shadow: var(--mainBoxShadow);
  }
  header a {
    padding: 25px;
    transition: 0.20s ease-in-out;
  }
  header a:hover {
    background-color: var(--brandingColor);
    color: #ffffff
  }
  header span {
    font-family: 'Caladea', serif;
    color: var(--brandingColor);
    margin-right: 25px;
  }
  .openedMenu {
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 100vw;
    background-color: #ffffff;
    position: fixed;
    bottom: 0px;
    left: 0px;
    box-shadow: var(--mainBoxShadow);
    animation-name: slideUp;
    animation-duration: 0.50s;
  }
  .openedMenu a {
    display: block;
  }
  .closedMenu {
    animation-name: slideUp;
    animation-direction: reverse;
    animation-duration: 0.50s;
  }
  .menuBtn {
    display: none;
    border: none;
    background-color: transparent;
    fill: var(--brandingColor);
  }

  @keyframes slideUp {
    from {
      height: 0vh;
    }
    to {
      height: 100%;
    }
  }

  @media screen and (max-width: 650px) {
    header {
      padding: 15px;
    }
    nav {
      display: none;
    }
    .menuBtn {
      display: initial;
    }
  }
</style>

<header>
  <button class="menuBtn" on:click={() => openMenu = !openMenu}>
    <svg style="width:24px;height:24px" viewBox="0 0 24 24">
      <path d="M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z" />
    </svg>
  </button>
  <span>Carpenter</span>
  <nav on:touchstart={e => touchStart(e)} on:touchmove={e => touchMove(e)} class={openMenu ? "openedMenu" : "closedMenu"}>
    {#each links as [url, name]}
    <a on:click={() => openMenu = false} href={url}>{name}</a>
    {/each}
  </nav>
</header>
<slot />
<footer>
  <a href="https://kevin-sheard.com/Impressum">Impressum</a>
  <a href="#Datenschutz">Datenschutz</a>
  <a href="#Kontakt">Kontakt</a>
</footer>