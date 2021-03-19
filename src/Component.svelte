<script>
  export let productId = "";
  export let text = "Buy my product!";
  export let offerDetails = null;
</script>

<svelte:head>
  <script src="https://gumroad.com/js/gumroad.js"></script>
</svelte:head>

<div class="cta">
  <a class="buy-button decor-font" href="https://gum.co/{productId}?wanted=true" target="_blank" data-gumroad-single-product="true">
    <h3>
      <svg x="0px" y="0px" viewBox="0 0 466.76 466.76" width="28" style="enable-background:new 0 0 466.76 466.76;" xml:space="preserve">
        <circle cx="363.52" cy="402.852" r="56.32" fill="#ffffff"/>
        <path d="M453.632,97.7c-1.536-0.512-3.072-0.512-4.608-0.512h-330.24l-14.848-75.264C102.4,13.732,94.72,7.588,86.528,7.588H0
            v35.84h71.68l53.248,267.776c1.536,8.192,9.216,14.336,17.408,14.336h256c8.192,0,15.36-5.632,17.408-13.312l50.176-192.512
            C468.992,109.988,463.36,100.26,453.632,97.7z" fill="#ffffff"/>
        <circle cx="164.352" cy="402.852" r="56.32" fill="#ffffff"/>
      </svg>
      {text}
    </h3>
    {#if offerDetails}
      <p>{offerDetails}</p>
    {/if}
  </a>
</div>

<style>
.cta {
  display: flex;
  align-content: center;
  justify-content: center;
  padding-top: 1em;
  padding-bottom: 1em;
}

.buy-button {
  border-radius: 6px;
  background-color: rgb(0, 189, 57);
  background-repeat: no-repeat;
  margin: 0.6em auto auto auto;
  padding: 0.8em 1.8em;
  transition-duration: 0.2s;
  overflow: hidden;
  box-shadow: none;
}

.buy-button:hover,
.buy-button:active,
.buy-button:focus  {
  box-shadow: inset 0 0px 0px 0 rgba(255,255,255,0.22),0 233px 233px 0 rgba(255,255,255,0.12) inset;
}

h3 {
  color: #fff;
  text-transform: uppercase;
  margin: 0 auto;
  font-size: 22px;  
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-content: center;
  flex-wrap: nowrap;
}

svg { 
  margin-right: 0.8em;
  position: relative top -2px;
}

p {
  color: #fff;
  font-weight: 300;
  text-align: center;
  font-size: 18px;
  margin: 6px 0 0 0;
}
</style>
