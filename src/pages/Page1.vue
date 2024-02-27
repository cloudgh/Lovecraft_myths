<template>
    <div class ="content">
        <!-- <my-header ></my-header> -->
        <h1>Мифы Лавкрафта</h1>
        <div class="container">  
            <img src="@/assets/people.jpg">
            <p class="text info">Даже самые страшные монстры, противостоящие героям фантастики, выполняют прозаичные функции:
                внезапно выскочить из темноты, укусить за самое чувствительное место и скрыться в никуда.
                Под этот шаблон подпадают вампиры, оборотни, призраки и зомби.
                Эти твари родились из мифов и легенд, суеверий и предрассудков, словом, человечество придумало их,
                чтобы обосновать свой естественный страх перед всем неожиданным и непонятным.<br><br>
                Но есть и другие легенды. Мифы о невероятных монстрах, гораздо более страшных, 
                чем кучка оживших мертвецов, и гораздо более загадочных, чем полупрозрачные существа,
                гуляющие по коридорам старинных замков. В отличие от европейских легенд, 
                эти истории не могут похвастать древностью. Их придумал один-единственный человек — нищий американец, 
                страдавший от ночных кошмаров. Но современная фантастика (а в особенности — мистика и ужасы)
                без них совершенно немыслима.</p>
            <div class="text ps">
                <p class="post">P.s на данном сайте представлены не все виды существ из разделов:</p> 
                <ul>
                    <li v-for="title in titles" :key="index">
                        {{ title }}
                    </li>
                </ul> 
            </div>  
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            titles: [
                "Древние", "Внешние боги", "Старшие боги", "Небожественные существа"
            ],
        }
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
    background-image: url("@/assets/background1.jpg");
    background-attachment: fixed;
    background-repeat: no-repeat;
    background-size: cover;
    font-size: 16pt;
    z-index: -1;
}
h1{
    display: flex;
    text-align: center;
    margin-top: 65px;
    justify-content: center;
}
.container {
    display: grid;
    grid-template-columns:  1fr 1.5fr;
    grid-template-rows: repeat(2, auto);
    grid-column-gap: 10px;
    grid-row-gap: 10px;
    @media (max-width: 768px) {
        grid-template-columns: 1fr;
        grid-template-rows: repeat(3, auto);
    } 
    img {
        width: clamp(200px,70%,400px);
        grid-row: span 2;
        object-fit: contain;
        margin: 0 auto;
    }
    .text{
        justify-self: center;
        align-self: center;
        width: 90%;
        background-color: #3b3b3c9a;
        padding: 20px;
    }
    .info {
        border-left: 4px solid #125471;
        border-bottom: 2px solid #125471;
    }
   

    .ps{
        border-right: 2px solid #1D3356; 
        border-bottom: 4px solid #1D3356; 
        margin-bottom: 10px;
        ul{
            padding-left: 25px;
        }
    }
}


</style>