<template>
    <div>
        <div class="col-md-12">
            <div class='page_container'>
                    <div class="row">
                        
                        <div class="card_container_sm" v-for="c in coins" :key="c.id">
                            <div class='card card01' :style="c.style">
                                <div class='card_category'>
                                    {{c.name}}
                                </div>
                                <b-button variant="warning" class="card_button">Detail</b-button>
                            </div>
                            </div>
                    </div>
            </div>
        </div>
    </div>
</template>
<script>
import axios from 'axios';
export default {
    data() {
        return {
            coins:[
                {id:'1',name:'Ethereum (ETH)',search:'ethereum',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://cdn.pixabay.com/photo/2018/09/07/09/10/ethereum-3660218_960_720.jpg)'},
                {id:'2',name:'Litecoin (LTC)',search:'litecoin',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://lh3.googleusercontent.com/proxy/iitni2U-zacNlq3Qa8N2-ml4NlL3yyRjS2rKZKuAyj0NbcWk2B1Ch09XsyOMbg7OPhz5UI3tYPSlRFZJJPww-CfptBj2AlWd3BsnWF1bTi4ms2Yn0l6c)'},
                {id:'3',name:'Cardano (ADA)',search:'cordano',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://www.coinkolik.com/wp-content/uploads/2021/02/cardano-ada.jpg)'},
                {id:'4',name:'Polkadot (DOT)',search:'polkadot',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://i2.wp.com/kriptokoin.com/wp-content/uploads/2020/08/polkadot-sale-1200x675-1.jpg?fit=770%2C433&ssl=1)'},
                {id:'5',name:'Bitcoin Cash (BCH)',search:'bitcoin',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://www.webtekno.com/images/editor/default/0002/56/fd60c6c5a3a4cb487677fcbb8d884f5fa883ec94.jpeg)'},
                {id:'6',name:'Stellar (XLM)',search:'stellar',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://stormgain.com/sites/default/files/news/Stellar%20Currency.jpg)'},
                {id:'7',name:'Chainlink',search:'chainlink',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://i1.wp.com/kriptokoin.com/wp-content/uploads/2020/08/Chainlink.jpg?fit=1200%2C780&ssl=1)'},
                {id:'8',name:'Binance Coin (BNB)',search:'binance-coin',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://www.coinkolik.com/wp-content/uploads/2019/09/Binance-Coin-BNB.jpg)'},
                {id:'9',name:'Tether (USDT)',search:'tether',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://media.cointral.com/wp-content/uploads/sites/2/2019/09/08014322/buy_tether.jpg)'},
                {id:'10',name:'Monero (XMR)',search:'monero',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://uzmancoin.com/wp-content/uploads/2020/10/monero-xmr.jpg)'},
                {id:'11',name:'Dogecoin (DOGE)',search:'dogecoin',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://iasbh.tmgrup.com.tr/fcbc7f/650/344/0/2/1280/673?u=https://isbh.tmgrup.com.tr/sbh/2021/01/29/dogecoin-nedir-ve-nasil-alinir-dogecoin-kac-tl-oldu-1611901812473.jpg)'},
                {id:'12',name:'Tether (USDT)',search:'tether',style:'background-color:rgba(54, 25, 25, .00004);background-image: url(https://i.ytimg.com/vi/9j5KqATrr3M/maxresdefault.jpg)'}
            ],
            apikey:'12900266-1f5815a23ec1f14f4c6b18e1e'
        }
    },
    mounted() {
        this.getImage()
    },
    methods: {
        getImage()
        { 
            for (const element of this.coins) {
                //console.log(element.name)
                let url = 'https://pixabay.com/api/?key='+this.apikey+'&q='+element.search+'&image_type=photo&pretty=true&min_width=200';
                axios.get(url).then(response=>{
                    if(response.data.hits.length > 0)
                    {
                        //this.coins.style = 'background-color:rgba(54, 25, 25, .00004);'+'background-image: url('+response.data.hits[0].largeImageURL+')';
                        console.log(response.data.hits[0].largeImageURL);
                    }
                    else
                    {
                        console.log('Error')
                    }
                });
            }
        }
    },
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
  font-size: 14px;
  font-weight: 400;
}
.card_button:active{
  color: #333;
}
.card_container_md .card_title{
  max-width: 40%;
}

</style>