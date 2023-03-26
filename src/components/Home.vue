<template>
    <div class="home">
        <div class="home__controll">
            <div v-for="(item, index) in Array(bannerLength)"
                :class="'home__controll-item ' + (bannerIndex == (index + 1) ? 'home__controll-item_active' : '')"
                @click="changeBanner(index + 1)" :key=index></div>
        </div>
        <div class="home__banner">
            <div :class="'home__banner-item ' + (bannerIndex == 1 ? 'home__banner-item_active' : '')">
                <div class="home__banner-inner">
                    <div class="home__text">
                        <div class="home__title">
                            Профессиональная поддержка
                        </div>
                        <div class="home__desc">
                            Найдите решения вместе с опытным психологом и достигните эмоционального равновесия
                        </div>
                    </div>
                    <div class="home__image"><img src="@/assets/img/banner-1.jpg" alt=""></div>
                </div>
            </div>
            <div :class="'home__banner-item ' + (bannerIndex == 2 ? 'home__banner-item_active' : '')">
                <div class="home__banner-inner">
                    <div class="home__text">
                        <div class="home__title">
                            Конфиденциальность гарантирована
                        </div>
                        <div class="home__desc">
                            Уверенность в сохранении конфиденциальности, гарантирует вам свободу от страхов и неприятностей
                        </div>
                    </div>
                    <div class="home__image"><img src="@/assets/img/banner-2.jpg" alt=""></div>
                </div>
            </div>
            <div :class="'home__banner-item ' + (bannerIndex == 3 ? 'home__banner-item_active' : '')">
                <div class="home__banner-inner">
                    <div class="home__text">
                        <div class="home__title">
                            Благоприятная атмосфера
                        </div>
                        <div class="home__desc">
                            Уютный кабинет и располагающая атмосфера создают условия для погружения во внутренний мир и
                            нахождения решений
                        </div>
                    </div>
                    <div class="home__image"><img src="@/assets/img/banner-3.jpg" alt=""></div>
                </div>
            </div>
            <div :class="'home__banner-item ' + (bannerIndex == 4 ? 'home__banner-item_active' : '')">
                <div class="home__banner-inner">
                    <div class="home__text">
                        <div class="home__title">
                            Личный подход
                        </div>
                        <div class="home__desc">
                            Мы придаем большое значение индивидуальным потребностям каждого клиента, чтобы достичь наилучших
                            результатов
                        </div>
                    </div>
                    <div class="home__image"><img src="@/assets/img/banner-4.jpg" alt=""></div>
                </div>
            </div>
            <div :class="'home__banner-item ' + (bannerIndex == 5 ? 'home__banner-item_active' : '')">
                <div class="home__banner-inner">
                    <div class="home__text">
                        <div class="home__title">
                            Социальная поддержка
                        </div>
                        <div class="home__desc">
                            Наши группы поддержки помогут вам общаться с людьми, которые сталкиваются с теми же проблемами,
                            и
                            дадут вам новые инсайты и взгляды
                        </div>
                    </div>
                    <div class="home__image"><img src="@/assets/img/banner-5.jpg" alt=""></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Home',
    methods: {
        changeBanner(index) {
            this.bannerIndex = index;
        }
    },
    data() {
        return {
            bannerIndex: 1,
            bannerLength: 0
        }
    },
    mounted() {
        this.bannerLength = document.querySelectorAll(".home__banner-item").length;
    }
}
</script>

<style scoped>
@import "@/assets/css/font-awesome.min.css";

.home {
    display: flex;
    align-items: center;
    justify-content: center;
}

.home__banner-item {
    height: 100vh;
    overflow: hidden;
    top: -100vh;
    position: absolute;
    width: 100%;
    left: 0;
}

.home__banner-inner {
    position: relative;
    height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.home__image {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
}

.home__banner-item_active {
    animation: bannerFade 2s;
    visibility: visible;
    top: 0;
}

@keyframes bannerFade {
    0% {
        top: -100vh
    }

    100% {
        top: 0;
    }
}

.home__banner-item_active .home__text {
    animation: textFade 2.8s;
}

@keyframes textFade {
    0% {
        opacity: 0;
        transform: translateY(-100px);
    }

    100% {
        opacity: 1;
        transform: translateY(0px);
    }
}

.home__banner img {
    width: 100%;
}

.home__text {
    position: relative;
    z-index: 1;
}

.home__controll {
    position: absolute;
    right: 20px;
    top: 50%;
    transform: translate(-50%);
    z-index: 1;
}

.home__controll-item {
    position: relative;
    width: 25px;
    height: 25px;
    border-radius: 100%;
    margin-bottom: 8px;
    border: solid 1px white;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition-duration: 0.4s;
}

.home__controll-item:hover:after {
    position: absolute;
    width: 7px;
    height: 7px;
    background: white;
    border-radius: 100%;
    content: '';
    transition-duration: 0.4s;
}

.home__controll-item_active:after {
    position: absolute;
    width: 7px;
    height: 7px;
    background: white;
    border-radius: 100%;
    content: '';
}

.home__title {
    font-family: 'Pattaya', sans-serif;
    color: white;
    text-align: center;
    margin-bottom: 20px;
    font-size: 30px;
}

.home__desc {
    text-align: center;
    max-width: 900px;
    margin: auto;
    color: white;
}

@media(max-width: 900px) {

    .home__banner img {
        height: 100%;
        width: unset;
    }

    .home__image {
        top: -40%;
        left: -231%;
    }

    .home__controll {
        display: flex;
        gap: 8px;
        top: unset;
        bottom: 110px;
    }

    .home__banner-item {
        padding: 0 20px;
    }

    .home__text {
        margin-bottom: 150px;
    }
}
</style>
