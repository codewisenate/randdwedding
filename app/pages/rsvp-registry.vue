<template>
  <div style='display: flex;'>
   <div style='width: 66%;'>
    <iframe
      src="https://www.online-rsvp.com/event/index.php?event_id=3852&embed=1&token=706b7dbb5fd2dcd69c6fb72562656e4e"
      style="min-height: 80vh; width: 100%; border: none;"
      title="Online RSVP event form"
      onload="this.style.height=(document.querySelector('.main').offsetHeight -
document.querySelector('header').offsetHeight -
document.querySelector('footer').offsetHeight)+'px';"
    ></iframe>
	</div>
    <div style='margin-top: 8rem;text-align: center; width: 33%;'>
	<hr />
	<p>If you would like to purchase an item off the registry, please indicate that it has been purchased on the registry item’s page by selecting “I have bought this gift already” for the convenience of other guests.</p>
      <button class='registry-btn'
        onclick="window.location = 'https://www.myregistry.com/wedding-registry/denielle-hill-and-rowan-king-vancouver-british-columbia/2556670'"
      ><i class="icon-present icons"></i>
        Visit the Gift Registry
      </button>
    </div>
  </div>
</template>


<style lang="scss">

p {
	color: rgb(82, 82, 82);
	font-size: 1.3rem;
}

hr {
  border: none;
  width: 60%;
  max-width: 400px;
  height: 50px;
  overflow: hidden;
  margin: 0 auto;
	&::after {
		content: '';
		display: block;
		margin: -30px auto 0;
		width: 100%;
		height: 25px;
		border-radius: 150px / 10px;
		box-shadow: 0 0 20px #ccc;
	}
}

.registry-btn {
	background-color: rgb(141,160,110);
	color: white;
	border-radius: 3px;
	padding: .75em 30px;
	display: inline-block;
	max-height: 55px;
	transition: all 0.2s;
	margin: 3rem auto 0;
	font-style: italic;

	&::before {
		content: "\e02f";
	  	font-family: simple-line-icons;
	  	margin-right: 6px;
	  	color: lightgray;
	  	transition: color 0.2s;
	  	font-style: normal;
	  	vertical-align: -1px;
	}
	
	&:hover {
		background-color: hsl(82, 20%, 42%);
		transform: translateY(-3px);
		vertical-align: -1px;
	}
}
</style>