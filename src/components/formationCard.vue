<template>
  <div class="formation--card">
    <div class="formation--image"></div>
    <div class="formation--information">
        <div class='top'>
            <p class="name">
                Openclassroom
            </p>
            <p class="description">
                Formation développeur web
            </p>
            <p class="time">
                6 mois
            </p>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "formationCard",
    props: {
        info_formation: Array
    }
}
</script>

<style lang="scss">
    .formation--card{
        width: 20%;
        height: 30%;
        .p{
            margin: 0px;
        }
        .formation--image{
            background-image: url('../assets/OClogo.jpeg');
            height: 70%;
            background-size: cover;
            background-position: center;
        }
        .formation--information{
            margin: 10px 0px;
            .top{
                margin-left: 9px;
                text-align: center;
            }
            .time{
                background-color: #f7f475;
                
            }
        }
    }
</style>