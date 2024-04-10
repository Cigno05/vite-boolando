<!-- JS -->
<script>

export default {


}
</script>

<!-- HTML -->

<template>
  <header>
        <nav class="navigation">
            <nav class="container page-header">
                <div class="row nav">
                    <ul class="col gender flex gap-5">
                        <li><a href="#">Uomo</a></li>
                        <li><a href="#">Donna</a></li>
                        <li><a href="#">Bambino</a></li>
                    </ul>
                    <div class="col logo">
                        <img src="../assets/boolean-logo.png" alt="logo boolean">
                    </div>
                    <ul class="col profile-app flex gap-5">
                        <li><a href="#">P</a></li>
                        <li><a href="#">H</a></li>
                        <li><a href="#">C</a></li>
                    </ul>
                </div>
            </nav>
        </nav>
    </header>
</template>

<!-- CSS -->

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

header {
    
    color: white;
    position: relative;
}

.navigation {
    
    background-color: $brand-orange;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 998;
    
}

.page-header .row {
    justify-content: space-between;
    max-height: 30px;
    align-items: center;
    padding: 0 10px;
}

.logo {
    
    img {
    max-height: 20px;
    }
}

</style>
