<script>
  import productDesktop from "$lib/images/image-product-desktop.jpg"
  import productMobile from "$lib/images/image-product-mobile.jpg"
  import cartIcon from "$lib/images/icon-cart.svg"
</script>

<article class="card">
  <section class="photo">
    <picture>
      <source media="(width >= 640px)" srcset={productDesktop} >
      <img src={productMobile} alt="Perfume" >
    </picture>
  </section>
  <section class="description">
    <h3 style="letter-spacing: 2px; font-weight: 500; color:var(--clr-neutral-2)">PERFUME</h3>
    <h1 style="font-size: xx-large; font-family: var(--ff-primary-2); font-weight:700">Gabrielle Essence Eau De Parfum</h1>
    <p style="color:var(--clr-neutral-2)">A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer Creator for House of CHANEL</p>
    <p class="price" ><span style="font-size: xx-large; font-family: var(--ff-primary-2); font-weight: 700; color:var(--clr-primary-1)">$149.99</span> <span style="font-weight: 500; color:var(--clr-neutral-2); font-size: small; text-decoration: line-through;">$169.99</span></p>
    <button>
      <img src={cartIcon} alt="add to cart" >
      Add to Card
    </button>
  </section>
</article>


<style>
  /* Layout Card*/
  .card{
    margin-inline: 1rem;
    /* margin-block: 3rem; */
    background-color: var(--clr-neutral-3);
    border-radius: 1rem;
    overflow: hidden;
    display: grid;
    grid-template-rows: 2fr 2.5fr;
    max-width: 25rem;
  }

  @media(width >= 640px) {
    .card {
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr;
      max-width: 40rem;
    }
  }

  .photo {
    /* border: 1px solid red; */
  }

  .description{
    display: grid;
    gap: 1rem;
    padding: 2rem;

  }



  /* Component */

    picture, img, source {
    /* display: block; */
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .price {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: start;
    gap: 1rem;
  }

  button {
    background-color: var(--clr-primary-1);
    display: grid;
    grid-template-columns: auto 1fr;
    padding: 1rem;
    border-radius: 1rem;
    color: var(--clr-neutral-3);
    font-weight: 700;
    border: transparent;
    
    /* margin-inline: 1rem; */
  }

  button:hover {
    /* background-color: var(--clr-primary-1); */
    filter: brightness(85%);
  }

  /* Typography */

</style>