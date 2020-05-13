<template>
    <div class="form">
        <form>
            <label for="firstName">Имя</label>
            <input type="text" id="firstName" v-model="firstName">
            <label for="lastName">Фамилия</label>
            <input type="text" id="lastName" v-model="lastName">
            <label for="patronymic">Отчество</label>
            <input type="text" id="patronymic" v-model="patronymic">
            <input type="submit" @click.prevent="send">
        </form>
    </div>
</template>

<script>
    export default {
        name: 'Form',
        data(){
            return{
                firstName: null,
                lastName: null,
                patronymic: null
            }
        },
        methods: {
            send(){
                const data = `${this.firstName} ${this.lastName} ${this.patronymic}`;
                console.log(data);
            }
        }
    }
</script>

<style lang="sass" scoped>
    .form
        margin: auto
        form
            display: flex
            flex-direction: column
            width: 307px
            label
                font-size: 30px
            input
                margin-bottom: 15px
                padding: 10px 5px
                outline: none
                transition: 0.5s
                border: 1px solid #000
                &:focus
                    color: #fff
                    background: #3D8144
                &[type="submit"]
                    display: flex
                    cursor: pointer
                    margin-left: auto
                    padding: 10px 40px
                    font-size: 18px
                    color: #fff
                    border: 1px solid #000
                    background: #3D8144
                    &:hover
                        background: #fff
                        color: #3D8144
</style>