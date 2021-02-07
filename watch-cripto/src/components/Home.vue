<template>
    <div>
        <div class="col-md-12">
            <div class='page_container'>
                    <div class="row">
                        
                        <div class="card_container_sm">
                        <div class='card card01'>
                            <div class='card_category'>
                            HILLARIOUS
                            </div>
                            <div class="card_title">
                            Is it Hilarious When Women Eat?
                            </div>
                            <a href='http://cards-ui-kit.webflow.io/' target="_blank" class="card_button">
                            Explore
                            </a>
                        </div>
                        </div>

                        <div class="card_container_sm">
                        <div class='card card02'>
                            <div class='card_category'>
                            INTRODUCTION
                            </div>
                            <div class="card_title">
                            5 Crazy Recent News Stories
                            </div>
                            <a href='http://cards-ui-kit.webflow.io/' target="_blank"  class="card_button">
                            Explore
                            </a>
                        </div>
                        </div>

                        <div class="card_container_md">
                        <div class='card card03'>
                            <div class='card_category dark'>
                            TRENDING
                            </div>
                            <div class="card_title dark">
                            Alton Attorney Accidentally Sues Himself
                            </div>
                            <a href='http://cards-ui-kit.webflow.io/' target="_blank"  class="card_button">
                            Explore
                            </a>
                        </div>
                        </div>
                    
                    </div>
                    <div class="row">
                        
                        <div class="card_container_md">
                        <div class='card card04'>
                            <div class='card_category dark'>
                            RICE ON THE RISE
                            </div>
                            <div class="card_title dark">
                            There's A Rice Deal Out There For Everyone
                            </div>
                            <a href='http://cards-ui-kit.webflow.io/' target="_blank"  class="card_button">
                            Explore
                            </a>
                        </div>
                        </div>
                        
                        <div class="card_container_sm">
                        <div class='card card05'>
                            <div class='card_category dark'>
                            SPORT
                            </div>
                            <div class="card_title dark">
                            Tiger Woods plays with own balls, Nike says
                            </div>
                            <a href='http://cards-ui-kit.webflow.io/' target="_blank" class="card_button">
                            Explore
                            </a>
                        </div>
                        </div>

                        <div class="card_container_sm">
                        <div class='card card06'>
                            <div class='card_category'>
                            COMEDY
                            </div>
                            <div class="card_title">
                            Are you Joey from Friends?
                            </div>
                            <a href='http://cards-ui-kit.webflow.io/' target="_blank"  class="card_button">
                            Explore
                            </a>
                        </div>
                        </div>
                        
                    </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.page_container{
  width: 940px;
  min-height: 400px;
  margin: auto;
  font-family: Roboto, sans-serif;
  color: #333;
}
.row{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-item: center;
  flex-direction: row;
  padding-top: 50px;
  padding-bottom: 50px;
}
.card_container_sm{
  width: 25%;
}
.card_container_md{
  width: 50%;
}
.card{
  height: 340px;
  margin: 10px;
  padding: 30px;
  border-radius: 8px;
}
.card01{
  position: relative;
  background-image: url(https://uploads-ssl.webflow.com/5ae109486d7b6097d347f1e3/5ae2268b7ceab455294d32b6_card1.jpg);
  background-position: 50% 50%;
  background-size: cover;
}
.card02{
  position: relative;
  background-image: url(https://uploads-ssl.webflow.com/5ae109486d7b6097d347f1e3/5ae2277ea95a89eb5b5d830e_card2.jpg);
  background-position: 50% 50%;
  background-size: cover;
}
.card03{
  position: relative;
  background-image: url(https://uploads-ssl.webflow.com/5ae109486d7b6097d347f1e3/5ae22b2a0663562314f7915f_card3.jpg);
  background-position: 50% 50%;
  background-size: cover;
}
.card04{
  position: relative;
  background-image: url(https://uploads-ssl.webflow.com/5ae109486d7b6097d347f1e3/5ae22e9c7ceab419284d3b61_card4%402x.jpg);
  background-position: 50% 50%;
  background-size: cover;
}
.card05{
  position: relative;
  background-image: url(https://uploads-ssl.webflow.com/5ae109486d7b6097d347f1e3/5ae22ea0a95a897b235d8bfa_card5%402x.jpg);
  background-position: 50% 50%;
  background-size: cover;
}
.card06{
  position: relative;
  background-image: url(https://uploads-ssl.webflow.com/5ae109486d7b6097d347f1e3/5ae22ea17b3f60de35084890_card6%402x.jpg);
  background-position: 50% 50%;
  background-size: cover;
}
.card_category{
  color: #fff;
  font-size: 12px;
  line-height: 20px;
  font-weight: 500;
  letter-spacing: 2px;
  text-transform: uppercase;
}
.card_title{
  color: #fff;
  margin-bottom: 10px;
  margin-top: 10px;
  font-size: 22px;
  line-height: 32px;
  font-weight: 400;
}
.card_category.dark{
  color: rgba(51, 51, 51, .4)
} 
.dark{
  color: #333;
}
.card_button{
  position: absolute;
  left: 30px;
  bottom: 30px;
  display: block;  
  padding-top: 9px;
  padding-bottom: 9px;
  padding-left: 25px;
  padding-right: 25px;
  text-align: center;
  border-radius: 4px;
  background-color: #fff;
  font-size: 14px;
  font-weight: 400;
  text-decoration: none;
  color: #333;
}
.card_button:active{
  color: #333;
}
.card_container_md .card_title{
  max-width: 40%;
}

</style>