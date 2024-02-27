<template>
    <div class ="content">
        <div class="container">  
            <h1 class="title">Отец Чудовищ</h1> 
            <img src="@/assets/autor2.png">
            <p>Говард Филлипс Лавкрафт (20.08.1890 — 15.03.1937) по праву считается одним из отцов жанра ужасов.
                Он взял многое от Эдгара По и лорда Дансени, но еще больше было взято у него.
                Клайв Баркер, Стивен Кинг, Ганс Руди Гигер, Нил Гейман, Гильермо Дель Торо, 
                Сэм Рэйми и Алан Мур не скрывают, что черпают вдохновение в творчестве человека,
                придумавшего легенду про «книгу мертвых» — «Некрономикон».
                Заслуга Лавкрафта ещё и в том, что он впервые скрестил два ранее независимых жанра —
                научную фантастику и ужасы. Говард создал масштабный пантеон из богов, 
                полубогов и чудовищ — существ потусторонних и одновременно реальных,
                обитающих то ли в другом измерении, то ли на других планетах, 
                но активно вмешивающихся в дела людей при помощи своих сверхъестественных сил.</p>
             
        </div>
    </div>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue';
export default {
    components:{
        MyHeader,
    },
    beforeRouteLeave(to, from, next) {
        window.scrollTo(0, 0);
        next();
    },
}
</script>

<style lang="scss" scoped>
.content{
    position: absolute;
    top:0;
    right: 0;
    color: #fff;
    min-width: 100vw;
    min-height: 100vh;
    background-image: url("@/assets/book1.png");
    background-attachment: fixed;
    background-repeat: no-repeat;
    background-size: cover;
    font-size: 16pt;
    z-index: -1;
}
.container{
    display: grid;
    grid-template-areas: "image content"
                        "label content";
    grid-template-columns:  1fr 1.1fr;
    grid-template-rows: repeat(2, auto);
    grid-column-gap: 10px;
    grid-row-gap: 10px;
    padding-top: 65px;
    @media (max-width: 768px) {
        grid-template-columns: 1fr;
        grid-template-rows: repeat(3, auto);
        grid-template-areas: "image"
                            "label"
                            "content";
    } 
    .title{
        margin: -2vw 5vw 0 auto;
        grid-area: label;
    }
    img{
        width: clamp(300px,57%,500px);
        grid-area: image;
        object-fit: contain;
        margin: 5vw 2vw 0 auto;
    }
   
    p{
        grid-area: content;
        margin: 5vw auto 0 2vw;
        padding: 10px 10px;
        background-color: #2324435d;
        font-size: 20pt;
        border-radius: 40px;
        width: 70%;
    }
}
</style>