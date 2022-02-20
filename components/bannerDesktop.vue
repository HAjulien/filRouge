<template>
    <div id="pageDesktop" >
        <header class="headerDesktop">
            <img src="" alt="">
<!-- menu grand format tablette  -->
            <nav class="menuDesktop  ">
                <ul class="menuLiens">
                    <li class="menuLien "> <p class="nuxtLink"> <NuxtLink to="/">ACCUEIL</NuxtLink>  </p> </li>
                    <li class="menuLien "> <p class="nuxtLink"> <NuxtLink to="/">MENU/TARIF</NuxtLink>  </p> </li>
                    <li class="menuLien "> <p class="nuxtLink"> <NuxtLink to="/">L'équipe</NuxtLink>  </p> </li>
                    <li class="menuLien "> <p class="nuxtLink"> <NuxtLink to="/">CLICK/COLLECT</NuxtLink>  </p> </li>
                    <li class="menuLien "> <p class="nuxtLink"> <NuxtLink to="/">CAFÉ</NuxtLink>  </p> </li>
                    <li class="menuLien "> <p class="nuxtLink"> <NuxtLink to="/">HORAIRE/LIEU</NuxtLink>  </p> </li>
                    <li class="menuLien "> <p class="nuxtLink"> <NuxtLink to="/">CONTACT</NuxtLink>  </p> </li>
                </ul>
            </nav>
        </header>
<!-- les images Accueil vont se succeder lors d une animation -->
        <section class="heroBanner">
            <div class="bigImage" id="un"></div>
            <div class="bigImage" id="deux"></div>
            <div class="bigImage" id="trois"></div>
<!-- bandeau menu et header -->
        
        <article class="insideBigImage">
                <h1>Cantine Miam</h1>
                <p>Venez vivre une expérience unique. La cantine comme vous ne l'avez jamais connue!!</p>
            </article>
        </section>
        </div>
</template>

<script>
export default {
  name: 'BannerDesktop',
}
</script>

<style lang="scss" scoped>

#pageDesktop{
  overflow-x: hidden;
}
.heroBanner {
      position: relative;
      height: 100vh;
      width: 100vw;
      /* petit effet parallax titre dans l'image */
      perspective: 1px;
      transform-style: preserve-3d;
    /* pour enlever les barres defilement à l'interieux image */
      overflow-y: scroll;
      overflow-x: hidden;
    }
    /* les 3 div bigImage qui contiennent chacune 1 image en background */
    .bigImage {
      position: absolute;
      height: 150vh;
      width: 100vw;
      transform-style: inherit;
      background-size: cover;
      background-position: center;
      /* donne effet parallax */
      transform: translateZ(-1px) scale(2);
    /* passe les image en arriere plan */
      z-index: -1;
    }

    /* filtre opacité */
    .bigImage::before {
      content: "";
      @include absolutePosition(0,0,0,0);
      background-color: rgba(0, 0, 0, 0.2);
    }

    /* images de fond qui vont se succéder  */
    #un {
      background-image: url(~/assets/images/burgers.jpg);
      animation: thirdappear 3s 7s;
    }

    #deux {
      background-image: url(~/assets/images/pizza.jpg);
      animation: Secondappear 3s 4s;
    }

    #trois {
      background-image: url(~/assets/images/festive.jpg);
      animation: firstappear 4s;
    }

    /* conteneur des textes dans image */
    .insideBigImage {
      position: absolute;
      top: 65%;
      left: 50%;
      height: 100vh;
      width: 100vw;
      transform: translate(-50%, -50%);
      text-align: center;
      color: white;
    }
    /* texte dans la grande image */

    .insideBigImage h1 {
      margin-bottom: 40vh;
      font-family: 'Roboto', sans-serif;
      font-weight: 800;
      font-size: 8rem;
      text-transform: uppercase;
      letter-spacing: 4px;
      /* contour couleur titre */
      -webkit-text-stroke: 4px #cda673;
      animation: showup 3s;
    }

    .insideBigImage p {
      font-size: 1.5rem;
      margin: 0 30%;
      /* contour lettre en couleur */
      text-shadow: 1.5px 0 0 #534F56, 1.5px 1.5px 0 #534F56, 0 1.5px 0 #534F56, -1.5px 1.5px 0 #534F56, -1.5px 0 0 #534F56, -1.5px -1.5px 0 #534F56, 0 -1.5px 0 #534F56, 1.5px -1.5px 0 #534F56;
    }

    /* debut du menu fixe en haut */
    .headerDesktop {
      position: fixed;
      top: 0;
      height: 37px;
      width: 100%;
      color: #f8f8f8;
      text-transform: lowercase;
      background: rgba(0, 0, 0, 0.7);
      z-index: 2;
    }

    .menuDesktop {
      position: absolute;
      top: 10%;
      right: 2%;
    }

    .menuLien {
      display: inline-block;
      width: 10vw;
    }

    .nuxtLink {
      display: flex;
      justify-content: center;
      align-content: center;
      font-size: .9rem;
    }

    .nuxtLink:hover {
      color: #cda673;
      transition: all .3s ease-in-out;
      transform: scale(1.3);
    }

   
   
    .menuLien:not(:last-child) {
      border-right: 2px solid #cda673;
    }

    .menuLien::after {
      content: "";
      display: block;
      margin: auto;
      height: 4px;
      margin-top: 5px;
      background-color: #cda673;
      transition: all .3s ease-in-out;
      transform: scale(0);
    }
    /* barre qui apparait sous menu lors d'un hover */

    .menuLien:hover::after {
      transform: scale(0.8);
      transition: all .3s ease-in-out;
    }

    /* animation titre qui se rempli */
    @-webkit-keyframes showup {
      0% {
        color: transparent;
      }
      40% {
        color: transparent;
      }
      100% {
        color: #f8f8f8;
      }
    }

    @keyframes showup {
      0% {
        color: transparent;
      }
      40% {
        color: transparent;
      }
      100% {
        color: #f8f8f8;
      }
    }

      /* animation image accueil qui se succede */
    @-webkit-keyframes firstappear {
      0% {
        transform: scale(1);
        z-index: 0;
      }
      20% {
        transform: scale(1);
        z-index: 0;
      }
      100% {
        transform: scale(1.1);
        z-index: 0;
      }
    }

    @keyframes firstappear {
      0% {
        transform: scale(1);
        z-index: 0;
      }
      20% {
        transform: scale(1);
        z-index: 0;
      }
      100% {
        transform: scale(1.1);
        z-index: 0;
      }
    }

    @-webkit-keyframes Secondappear {
      0% {
        transform: scale(1);
        z-index: 0;
      }
      20% {
        transform: scale(1);
        z-index: 0;
      }
      100% {
        transform: scale(1.1);
        z-index: 0;
      }
    }

    @keyframes Secondappear {
      0% {
        transform: scale(1);
        z-index: 0;
      }
      20% {
        transform: scale(1);
        z-index: 0;
      }
      100% {
        transform: scale(1.1);
        z-index: 0;
      }
    }

    @-webkit-keyframes thirdappear {
      0% {
        transform: scale(1);
        z-index: 0;
      }
      20% {
        transform: scale(1);
        z-index: 0;
      }
      100% {
        transform: scale(1.1);
        z-index: 0;
      }
    }

    @keyframes thirdappear {
      0% {
        transform: scale(1);
        z-index: 0;
      }
      20% {
        transform: scale(1);
        z-index: 0;
      }
      100% {
        transform: scale(1.1);
        z-index: 0;
      }
    }

    @media screen and (max-width:766px){
        #pageDesktop{
          display: none;
        }
    }


  @media screen and (min-width:766px) and (max-width:1024px) {

    /* on change les tailles des case du menu */
/* petites case pour accueil/cafe/equipe/contact */
    .menuLien:nth-child(odd){
        width: 10vw;
    }
/* grande cases pour les autres */
    .menuLien:nth-child(even){
        width: 15vw;
    }
  }
  
</style>