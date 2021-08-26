<style>
  section {
    width: 60vw;
    position: relative;
    margin: auto;
    background-image: url('../images/backgroundForm.svg');
    background-size: contain;
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: center;
  }
  form {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    margin: auto;
    top: 50%;
    padding: 5vw;
  }
  label {
    display: flex;
    flex-direction: column;
    margin: 15px 5px;
  }
  .textInputs {
    display: flex;
    flex-direction: row;
  }
  input, textarea {
    border-radius: var(--mainRadius);
    border: none;
    box-shadow: var(--mainBoxShadow);
    padding: 10px;
    background-color: #ffffff;
    width: auto;
    transition: 0.20s;
    transform-origin: left;
    border: 1px transparent solid;
  }
  input:hover, textarea:hover {
    border: 1px var(--brandingColor) solid;
  }
  input:focus, textarea:focus {
    border: 1px var(--brandingColor) solid;
    outline: unset;
  }
  input[type="submit"] {
    font-family: 'Caladea', serif;
    font-size: 1.2em;
  }
  input[type="submit"]:hover {
    cursor: pointer;
  }
  textarea {
    height: 150px;
    resize: none;
  }

  @media screen and (max-width: 800px) {
    .textInputs {
      flex-direction: column;
    }
    section {
      background-image: none;
      width: 90vw;
    }
  }
</style>

<section>
  <form>  
    <label>Schicken Sie uns eine unverbindliche Anfrage
      <textarea placeholder="..."></textarea>
    </label>
    <div class="textInputs">
      <label>Name:
        <input placeholder="..." type="text" />
      </label>
      <label>Email-Adresse:
        <input placeholder="..." type="email" />
      </label>
    </div>
    <label>
      <input type="submit" value="SENDEN" />
    </label>
  </form>
</section>