<!-- JS -->
<script>

export default {
    data() {
        return {
            currentIndex: 0,
            gendersArray: ['Uomo', 'Donna', 'Bambino'],
            actionsArray: ['Contatti', 'Store', 'Offerte']
        };
    },
    
}
</script>

<!-- HTML -->

<template>
  <header>
        <nav class="navigation">
            <nav class="container page-header">
                <div class="row nav">
                    <div class="gender-list">
                        <ul class="col gender flex gap-5" v-for="(gender) in gendersArray">
    
                            <li><a href="#">{{ gender }}</a></li>
                            
                        </ul>
                    </div>

                    <div class="col logo">
                        <img src="../assets/boolean-logo.png" alt="logo boolean">
                    </div>

                    <div class="action-list">
                        <ul class="col profile-app flex gap-5" v-for="(action) in actionsArray">
    
                            <li><a href="#">{{ action }}</a></li>
                            
                        </ul>
                    </div>
                    
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

.page-header {

    .row {
        justify-content: space-between;
        max-height: 30px;
        align-items: center;
        padding: 0 10px;
    }
}

.gender-list,
.action-list {
    display: flex;
    flex-direction: row;
    gap: 10px;
}

.logo {
    
    img {
    max-height: 20px;
    }
}

</style>
