<template>



<div id="backdrop">

<div id="backdrop-menu">
    <div class="container">
        LOGO
    </div>
</div>

<div class="container d-flex justify-content-center">

    <!--
    <div id="profil-card" class="shadowed d-flex">
        <img src="../assets/images/backdrop-pp.png" />
        
        <div id="profil-desc">
            <span>RIHANE Samy</span>
            <br />
            <span>Product Owner</span>
        </div>
        
    </div>
    -->

    <div class="row">

        <div class="col d-flex justify-content-center">
            <img id="pp_profil" src="../assets/images/backdrop-pp.png" />
        </div>

        <div class="col">
            <div class="text-journal">RIHANE Samy <img src="../assets/images/france.png" width="30"/></div>
            <br />
            <div class="text-journal">Product Owner</div>
            <div class="text-journal">Project Manager</div>
            <br />
            <div class="text-journal">Developer</div>
        </div>

    </div>


</div>

</div>

</template>

<script>


export default {
    name: "Home",
    
    data() {
        return {
            data: "",
        }
    },
    components: {

    },

    computed: {

    },

    methods: {

    }

}

</script>

<style>
#backdrop-menu {
    background-color: #224886;
    height: 50px;
}

#backdrop {
    background-color: #224886;
    width: 100%;
    height: 50vh;
}

#pp_profil {
    width: 250px;
    float: right;
    border-radius: 50%;
}

.text-journal {
    font-family: Anton;
    font-size: 1.8em;

    display: inline-block;
    color: #224886;
    background-color: white;

    padding: 10px;
    margin: 1px;
}

</style>