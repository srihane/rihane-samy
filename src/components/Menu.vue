<template>

<div class="fixed-bottom d-flex justify-content-center">
    <button class="btn-menu" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasWithBackdrop" aria-controls="offcanvasWithBackdrop"><i class="fa-solid fa-bars"></i> Menu</button>
</div>

<div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasWithBackdrop" aria-labelledby="offcanvasWithBackdropLabel">
  <div class="offcanvas-header">
    <!--<h5 class="offcanvas-title" id="offcanvasWithBackdropLabel">Offcanvas with backdrop</h5>-->
    <!--<button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>-->
    <div class="backdrop-sidenav">

        <div class="container">
            <div>
                <img src="../assets/images/backdrop-pp.png" class="backdrop-pp" /> 
            </div>

                <br />
                <div>
                    <span class="text-white">RIHANE Samy | <span style="text-decoration: underline;">Product Owner</span></span>
                </div>
                <div>
                    <span class="text-white">Entreprise actuel : <img src="../assets/images/free-logo.png" width="90" /></span>
                </div>

                <div style="margin-top: 20px !important;">
                    <span class="text white"><i class="fa-regular fa-envelope"></i> <a class="text-white" href="mailto:rihane.samy@icloud.com">rihane.samy@icloud.com</a></span>
                </div>
                <br />

        </div>

    </div>

  </div>

    <div class="side-menu">

        <!--
        <router-link to="/tchat">
        <div class="side-menu-link"><div class="container"><i class="fa-solid fa-comments"></i> Tchat</div></div>
        </router-link>
        -->

        <a href="#">
        <div class="side-menu-link"><div class="container">Articles</div></div>
        </a>

        <a href="#">
        <div class="side-menu-link"><div class="container">Projets</div></div>
        </a>

        <a href="#">
        <div class="side-menu-link"><div class="container">Recommandations</div></div>
        </a>

    </div>

  <div class="offcanvas-body">

    <div>
        <h4>Social</h4>
        <ul class="nav">
            <li class="nav-item">
                <a class="nav-link text black" aria-current="page" href="https://www.linkedin.com/in/samy-rihane-b33898115/" target="_blank"><i class="fa-brands fa-linkedin fa-2x"></i></a>
            </li>
            <li class="nav-item">
                <a class="nav-link text black" href="https://medium.com/@rihane.samy" target="_blank"><i class="fa-brands fa-medium fa-2x"></i></a>
            </li>
            <li class="nav-item">
                <a class="nav-link text black" href="https://github.com/srihane" target="_blank"><i class="fa-brands fa-github fa-2x"></i></a>
            </li>
        </ul>
    </div>

  </div>
</div>



</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>