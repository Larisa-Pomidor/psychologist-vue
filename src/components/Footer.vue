<template>
    <footer>
        <div class="footer__outer">
            <div class="container">
                <div class="footer__inner">
                    <div class="footer__copy">
                        This template is made with love by <b> LarisaPomidor.2SPL </b> <br> Copyright @2023 All rights reserved
                    </div>
                    <div class="footer__socials">
                        <a href="#" class="socials__item">
                            <i class="fa fa-twitter" aria-hidden="true"></i>
                        </a>
                        <a href="#" class="socials__item">
                            <i class="fa fa-telegram" aria-hidden="true"></i>
                        </a>
                        <a href="#" class="socials__item">
                            <i class="fa fa-youtube" aria-hidden="true"></i>
                        </a>
                        <a href="#" class="socials__item">
                            <i class="fa fa-pinterest" aria-hidden="true"></i>
                        </a>
                        <a href="#" class="socials__item">
                            <i class="fa fa-instagram" aria-hidden="true"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
.footer__outer {
    position: absolute;
    width: 100%;
    background: white;
    content: '';
    bottom: 0;
    left: 0;
    z-index: 2;
    padding: 10px 0;
}

.footer__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 100px;
}

.footer__copy {
    font-size: 12px;
    letter-spacing: 2px;
    font-weight: 700;
}

.footer__socials {
    display: flex;
    align-items: center;
    gap: 17px;
    position: relative;
    z-index: 2;
}

.socials__item {
    font-size: 16px;
    color: black;
    opacity: 0.9;
}
</style>
