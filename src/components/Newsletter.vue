<template>
	<Card class="newsletter" id="mc_embed_signup">
		<p class="mb-half text-center"><strong>👋 Jangan lewatkan setiap moment.</strong> Subscribe yuk!</p>
		<form action="https://340beff8.sibforms.com/serve/MUIEAGHhWFfDLb-mxEMnXwvvq7giKui45dtzvk0qcytCOQ3cyK-TypQwW3UdULPA4n5Ek4G5yGiWNW9tuiVB_CE6iFaA1VqWi3F44w5tjkJsR6IKI-nNh42K-H3qM3hTOw-UwqbyFkBXnQYze1pRAEhEiPZVZt_K-VRi0tL34mxerYhCfItSMnW6aMS9FGahqpH00EEHnKUcUq8n" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="newsletter__form validate" target="_blank" novalidate>
		<div id="mc_embed_signup_scroll" class="flex">
			
			<div class="newsletter__button">
				<button type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button primary">
					Subscribe
				</button>
			</div>

			<div id="mce-responses" class="clear">
				<div class="response" id="mce-error-response" style="display:none"></div>
				<div class="response" id="mce-success-response" style="display:none"></div>
			</div>
	  	<div style="position: absolute; left: -5000px;" aria-hidden="true">
	  		<input type="text" name="b_960a357f3405a688ff935a10e_42bbd30818" tabindex="-1" value="">
	  	</div>
	   </div>
		</form>
		<div class="newsletter__top"></div>
	</Card>
</template>

<style lang="scss">
.newsletter {
	
  &__top {
  	height: 4px;
  	position: absolute;
  	top:0;
  	left:0;
  	right:0;
  	background: linear-gradient(90deg, var(--primary-color) 40%,  #f37052 30%, #f7aa8e 20%, #fce6db 10%);
  }

  &__form {
  	margin-bottom:0;
  }
  &__field {
  	min-width: 200px;
  	margin-bottom: 1rem;
  }
  &__button {
  	margin: 0 auto;
  	margin-bottom: .2rem;
  }
  
  p {
  	margin-bottom: .5rem;
  }
}
</style>