<script>
  export let direction;

  let degrees = 0;

  console.log(direction);

  switch (direction) {
    case 'left':
      degrees = 180;
    break;

    case 'right':
      degrees = 0;
    break;
    
    case 'up':
      degrees = -90;
    break;

    case 'down':
      degrees = 90;
    break;
  }

  console.log(degrees);
</script>

<svg style="transform: rotate({degrees}deg)" xmlns="http://www.w3.org/2000/svg" width="68.267" height="119.411" viewBox="0 0 68.267 119.411">
  <path id="Icon_ionic-ios-arrow-back" data-name="Icon ionic-ios-arrow-back" d="M31.83,65.883,77.012,20.737A8.534,8.534,0,0,0,64.925,8.686L13.736,59.84a8.517,8.517,0,0,0-.249,11.766l51.4,51.509a8.534,8.534,0,0,0,12.086-12.051Z" transform="translate(79.518 125.604) rotate(180)" fill="#fff"/>
</svg>