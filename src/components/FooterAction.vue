<!-- JS -->
<script>

export default {

}
</script>

<!-- HTML -->

<template>
  <footer>
        <div class="container footer-nav">
            <div class="row">
                <div class="col footer-info">
                    <h3>Booleando s.r.l.</h3>
                    <ul class="flex gap-5">
                        <li><a href="#">Info Legali</a></li>
                        <li><a href="#">Info Privacy</a></li>
                        <li><a href="#">Diritto di recesso</a></li>
                    </ul>
                </div>
                <div class="col">
                    <h4>Trovaci anche su:</h4>
                    <ul class="footer-social flex gap-5">
                        <li><img src="../assets/twitter.png" alt="" class="footer-icon"></li>
                        <li><img src="../assets/instagram.png" alt="" class="footer-icon"></li>
                        <li><img src="../assets/facebook.png" alt="" class="footer-icon"></li>
                        <li><img src="../assets/youtube.png" alt="" class="footer-icon"></li>
                    </ul>
                </div>
            </div>
        </div>

    </footer>
</template>

<!-- CSS -->

<style lang="scss">

footer {
    background-color: #1A1A1A;
    color: white;
}



.footer-social {
    
    height: 15px;
}

.footer-nav {
    
    .row {
        justify-content: space-between;
        padding: 0 10px;
    }
}

.footer-icon {
    height: 24px;
}

</style>
