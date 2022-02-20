<template>
    <header class="headerDesktop">
        <img src="" alt="">
<!-- menu grand format tablette  -->
        <nav class="menuDesktop  ">
            <ul class="menuLiens">
                <li class="menuLien "> <NuxtLink to="/" class="nuxtLink" >ACCUEIL</NuxtLink> </li>
                        <li class="menuLien "> <NuxtLink to="/" class="nuxtLink" >MENU/TARIF</NuxtLink> </li>
                <li class="menuLien "> <NuxtLink to="/" class="nuxtLink" >L'équipe</NuxtLink> </li>
                <li class="menuLien "> <NuxtLink to="/" class="nuxtLink" >CLICK/COLLECT</NuxtLink> </li>
                <li class="menuLien "> <NuxtLink to="/" class="nuxtLink" >CAFÉ</NuxtLink> </li>
                <li class="menuLien "> <NuxtLink to="/" class="nuxtLink" >HORAIRE/LIEU</NuxtLink> </li>
                <li class="menuLien "> <NuxtLink to="/" class="nuxtLink" >CONTACT</NuxtLink> </li>
            </ul>
        </nav>
    </header> 
</template>

<script>
export default {
    name:'HeaderDesktop'
}
</script>

<style>
    .headerDesktop {
      display: flex;
      justify-content: flex-end;
      align-items: center;
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
      top: 10%;
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


    @media screen and (max-width:766px){
        .headerDesktop{
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