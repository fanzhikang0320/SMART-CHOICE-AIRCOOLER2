<template>
  <div class="product-wrapper">
      <div :class="{'product-item': true, 'first-item': index == 0, 'last-item': index == productList.length - 1}" v-for="(product,index) in productList" :key="index">
          <div class="circle" v-if="index != productList.length- 1">
              <span class="num">{{index + 1}}</span>
          </div>
          <div class="corner-box" v-if="index == 0">
              <span class="text">50% Discount Today!</span>
          </div>
          <div class="big-title" v-if="index == productList.length - 1">The Most Popular Portable Air Coolers Device In 2020</div>
          <a :href="product.link" target="_blank" class="product-link-box">
            <div class="product-container">
                <div class="product-container-left">
                    <div class="picture-box">
                        <img :src="product.picture" :alt="product.name" class="picture">
                    </div>
                    <div class="desc-list-box">
                        <h2 class="product-name">{{product.name}}</h2>
                        <ul class="list-box">
                            <li v-for="(item,id) in product.list" :key="id">
                                <span class="icon"></span>
                                <p class="text">{{item.text}}</p>
                            </li>
                        </ul>
                        <p class="buys" v-if="index == 0 || index == productList.length - 1"><span class="red">Limited Time Offer: </span><span class="text">Get 50% OFF plus Free Delivery</span></p>
                    </div>
                </div>
                <div class="product-container-right">
                    <p class="good">
                        <span class="text">{{index == 0 || index == productList.length - 1 ? 'Excellent': index == 1 ? 'Very Good': 'Good'}}</span>
                        <span class="king-icon" v-if="index == 0 || index == productList.length - 1"></span>
                        <span class="good-icon" v-if="index == 1"></span>
                    </p>
                    <p class="rate-box"><span class="score">{{product.rate}}</span><span>/10</span></p>
                    <a :href="product.link" target="_blank" class="btn">
                        <span class="text">Visit Site</span>
                        <span class="icon"></span>
                    </a>
                    <!-- <a :href="product.reviewLink" class="review">Read Our Review</a> -->
                </div>
            </div>
          </a>
      </div>
      
  </div>
</template>

<script>
export default {
    data() {
        return {
            productList: [
                {
                    id: 1,
                    name: 'Blaux',
                    picture: require('../assets/image/air/blaux.png'),
                    logo: require('../assets/image/air/blauxLogo.png'),
                    link: '/airDetail',
                    reviewLink: 'https://www.frstbte.com/7QLQCMW/5B6Z3NT/?uid=7012',
                    rate: '9.8',
                    desc: '<p style="font-size:20px;"><strong><span style="color:#F96E35;">Limited Time Offer: </span>Get 50% OFF plus Free Delivery</strong></p>',
                    list: [
                        {
                            text: 'Keeps large rooms super cool'
                        },
                        {
                            text: 'Long last battery life'
                        },
                        {
                            text: 'Unbeatable low price'
                        },
                        {
                            text: 'Advanced proximity motion sensor'
                        },
                        {
                            text: 'Cord-free operation'
                        },
                        {
                            text: 'Build-in water tank lasts up to 8 hours'
                        },
                        {
                            text: 'Three-speed personal space air humidifier'
                        },
                        {
                            text: 'Advanced proximity motion sensor'
                        },
                        {
                            text: 'Low noise'
                        },
                        {
                            text: '30-Day Money Back Guarantee'
                        }
                        
                    ]
                },
                {
                    id: 2,
                    name: 'UV Cooler',
                    picture:  require('../assets/image/air/UVC.png'),
                    logo: require('../assets/image/air/UVCLogo.png'),
                    link: 'https://uvcoolershop.com?widipub_id=5f07f06db7bb81096719fce3&amp;wtrd_offer_id=5ed67e3e824e0b59e570f103&amp;wtrd_offer_lids[]=5ed67e7098442f184e377e32&amp;_locale=en',
                    reviewLink: 'https://uvcoolershop.com?widipub_id=5f07f06db7bb81096719fce3&amp;wtrd_offer_id=5ed67e3e824e0b59e570f103&amp;wtrd_offer_lids[]=5ed67e7098442f184e377e32&amp;_locale=en',
                    rate: '9.6',
                    desc: '<p style="font-size:20px;"><strong><span style="color:#F96E35;">Limited Time Offer: </span>Get 50% OFF plus Free Delivery</strong></p>',
                    list: [
                        {
                            text: 'Small and light with UV sterilizer'
                        },
                        {
                            text: 'Long working mode for night time up to12h'
                        },
                        {
                            text: 'Easy to use'
                        },
                        {
                            text: 'Freon free, cools down spaces using just water and ice'
                        },
                        {
                            text: 'Silent working mode'
                        },
                        {
                            text: 'Perfect for room and desk air conditioning'
                        }
                    ]
                },
                {
                    id: '3',
                    name: 'CoolAir',
                    picture: require('../assets/image/air/coolair.png'),
                    logo: require('../assets/image/air/coolairLogo.png'),
                    link: 'https://hyperstech.com/coolair/order.php?net=9785&aff={AFFID}&sid={SUBID}&cid={CLICKID}',
                    reviewLink: 'https://hyperstech.com/intl_5/order.php?prod=coolair&net=9785&aff={AFFID}&sid={SUBID}&cid={CLICKID}',
                    rate: '9.6',
                    desc: '<p style="font-size:20px;"><strong><span style="color:#F96E35;">Limited Time Offer: </span>Get 50% OFF plus Free Delivery</strong></p>',
                    list: [
                        {
                            text: 'Fast cooling mode'
                        },
                        {
                            text: 'Sleep mode to use during the night'
                        },
                        {
                            text: 'Can cool, humidify and purify the air'
                        },
                        {
                            text: 'It can be powered via a USB port'
                        }
                    ]
                },
                {
                    id: 4,
                    name: 'Arcticbreeze',
                    picture: require('../assets/image/air/arcticbreeze.png'),
                    logo: require('../assets/image/air/arcticbreezeLogo.png'),
                    link: 'https://www.esplma.com/7QLQCMW/5GTH4TX/?uid=7574',
                    reviewLink: 'https://hypertechx.com/ps/freshr/index.php?net=9785&aff={AFFID}&sid={SUBID}&cid={CLICKID}',
                    rate: '9.5',
                    desc: '',
                    list: [
                        {
                            text: 'Cools areas up to 30 square meters effectively'
                        },
                        {
                            text: 'Easy to use'
                        },
                        {
                            text: 'Silent working mode'
                        },
                        {
                            text: 'Perfect for room and desk air conditioning'
                        }
                    ]
                },
                {
                    id: 5,
                    name: 'Blaux Personal fan',
                    picture:  require('../assets/image/air/blauxpersonalfan.png'),
                    logo: require('../assets/image/air/blauxLogo.png'),
                    link: 'https://www.frstbte.com/7QLQCMW/5723JL1/?uid=6580',
                    reviewLink: 'https://www.frstbte.com/7QLQCMW/5C5BTND/?uid=7119',
                    rate: '8.5',
                    desc: '',
                    list: [
                        {
                            text: 'Wearable personal  AC'
                        },
                        {
                            text: 'Keep cool anywhere'
                        },
                        {
                            text: 'One size fits all'
                        },
                        {
                            text: '3 fan speed modes'
                        },
                        {
                            text: 'LED ring to indicate power and charging status'
                        },
                        {
                            text: '30 hours runtime'
                        }
                    ]
                },
                {
                    id: 1,
                    name: 'Blaux',
                    picture: require('../assets/image/air/blaux.png'),
                    logo: require('../assets/image/air/blauxLogo.png'),
                    link: '/airDetail',
                    reviewLink: 'https://www.frstbte.com/7QLQCMW/5B6Z3NT/?uid=7012',
                    rate: '9.8',
                    desc: '<p style="font-size:20px;"><strong><span style="color:#F96E35;">Limited Time Offer: </span>Get 50% OFF plus Free Delivery</strong></p>',
                    list: [
                        {
                            text: 'Keeps large rooms super cool'
                        },
                        {
                            text: 'Long last battery life'
                        },
                        {
                            text: 'Unbeatable low price'
                        },
                        {
                            text: 'Advanced proximity motion sensor'
                        },
                        {
                            text: 'Cord-free operation'
                        },
                        {
                            text: 'Build-in water tank lasts up to 8 hours'
                        },
                        {
                            text: 'Three-speed personal space air humidifier'
                        },
                        {
                            text: 'Advanced proximity motion sensor'
                        },
                        {
                            text: 'Low noise'
                        },
                        {
                            text: '30-Day Money Back Guarantee'
                        }
                        
                    ]
                }
            ]
        }
    }

}
</script>

<style lang="less" scoped>
@import url('../assets/css/wifi-product.less');
</style>