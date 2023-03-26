<template>
    <div :class="'sidebar ' + (sidebarActive ? 'sidebar_active' : '')">
        <div class="sidebar__outer">
            <div class="sidebar__controll" @click="toggleSidebar">
                Связаться со мной
                <div class="sidebar__pen">
                    <i class="fa fa-pencil"></i>
                </div>
            </div>
            <div class="sidebar__inner">
                <form class="form">
                    <div class="form__name">
                        <input type="text" placeholder="Ваше имя" />
                    </div>
                    <div class="form__text">
                        <textarea type="text" rows="4" placeholder="Ваш комментарий" />
                    </div>
                    <div class="form__button"><button>Отправить</button></div>
                    <div class="form__privacy">
                        Ваши данные в сохранности, не передаются третьим лицам
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Sidebar',
    data() {
        return {
            sidebarActive: false
        }
    },
    methods: {
        toggleSidebar() {
            this.sidebarActive = !this.sidebarActive;
        }
    }
}
</script>

<style scoped>
form {
    margin-top: 70px;
}

.form__button button {
    padding: 10px;
    border-radius: 5px;
    width: 100%;
    background: black;
    color: white;
}

input,
textarea {
    width: 100%;
    margin-bottom: 10px;
    border-radius: 5px;
    outline: none;
    border: solid 1px silver;
    padding: 10px;
    font-weight: 700;
}

input::placeholder,
textarea::placeholder,
button {
    font-size: 14px;
    font-family: 'Poiret One', cursive;
}

.sidebar {
    position: fixed;
    right: -500px;
    top: 0;
    height: 100%;
    background: white;
    z-index: 1;
    transition-duration: 0.4s;
}

.sidebar_active {
    right: 0;
}

.sidebar__outer {
    padding: 0 40px;
    width: 300px;
}

.form__privacy {
    text-align: center;
    margin-top: 20px;
    font-weight: 700;
    font-size: 11px;
    letter-spacing: 2px;
}

.sidebar__controll {
    cursor: pointer;
    text-align: end;
    position: fixed;
    right: 40px;
    top: 11px;
    font-size: 16px;
    font-weight: 700;
    display: flex;
    align-items: center;
}

.sidebar__controll i {
    margin-left: 10px;
}
</style>
