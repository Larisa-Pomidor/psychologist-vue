<template>
    <div class="home">
        <div class="home__controll">
            <div class="home__controll-item home__controll-item_active"></div>
            <div class="home__controll-item"></div>
            <div class="home__controll-item"></div>
            <div class="home__controll-item"></div>
            <div class="home__controll-item"></div>
        </div>
        <div class="home__banner">
            <div class="home__banner-item home__banner-item_active">
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
            <div class="home__banner-item">
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
            <div class="home__banner-item">
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
            <div class="home__banner-item">
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
            <div class="home__banner-item">
                <div class="home__text">
                    <div class="home__title">
                        Социальная поддержка
                    </div>
                    <div class="home__desc">
                        Наши группы поддержки помогут вам общаться с людьми, которые сталкиваются с теми же проблемами, и
                        дадут вам новые инсайты и взгляды
                    </div>
                </div>
                <div class="home__image"><img src="@/assets/img/banner-5.jpg" alt=""></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Home'
}
</script>

<style scoped>
@import "@/assets/css/font-awesome.min.css";
.home {
    position: relative;
}

.home__banner-item {
    height: 100vh;
    overflow: hidden;
    display: none;
    position: relative;
}

.home__image {
    position: absolute;
    top: 0;
    left: 0;
}

.home__banner-item_active {
    display: flex;
    align-items: center;
    justify-content: center;
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
</style>
