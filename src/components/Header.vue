<template>
    <header>
        <div class="header__outer">
            <div class="container">
                <div class="header__inner">
                    <div class="header__logo">
                        Душевная Гармония
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped>
.header__outer {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1;
    content: '';
    background: white;
    padding: 10px 0;
}

.header__inner {
    display: flex;
    align-items: center;
}

.header__logo {
    font-family: 'Pattaya', sans-serif;
    font-size: 18px;
}

.header__menu-item {
    cursor: pointer;
    font-weight: 700;
}

@media(max-width: 900px) {

    .header__logo {
        font-size: 16px;
    }
}
</style>
