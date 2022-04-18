<template>
<div class="container">
  <Navbar />
  <Filters />
  <Products :items="items" />
  <Dash />
</div>
</template>

<script>

import Navbar from './components/Navbar.vue'
import Dash from './components/Dash.vue'
import Products from './components/Products.vue'
import Filters from './components/Filters.vue'
export default {
  name: 'App',
  components: { Navbar, Dash, Products, Filters },
  data (){
    return {
      items: [
        {
            "id":1,
            "name": "Apple Watch Series 5",
            "price": 339.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/1.3b312012.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":2,
            "name": "Apple iPhone 11 (64GB, Black)",
            "price": 669.99,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/2.1aba2cea.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":3,
            "name": "Apple iMac 27-inch",
            "price": 999.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/3.29c766f8.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":4,
            "name": "OneOdio A71 Wired Headphones",
            "price": 49.99,
            "rating": 3,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/4.73f34744.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":5,
            "name": "Apple - MacBook Air® (Latest Model) - 13.3 Display - Silver",
            "price": 999.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/5.c5b188e5.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":6,
            "name": "Switch Pro Controller",
            "price": 429.99,
            "rating": 3,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/6.833c8951.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":7,
            "name": "Google - Google Home - White/Slate fabric",
            "price": 129.29,
            "rating": 4,
            "img": "	https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/7.2a004c66.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "google",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":8,
            "name": "Sony 4K Ultra HD LED TV",
            "price": 7999.99,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/8.c170e8ca.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":9,
            "name": "OnePlus 7 Pro",
            "price": 14.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/9.3170c803.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Philips",
            "available": true,
            "colors": ["red", "purple", "green"]
        }
      ],
    }
  }
  
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@500&family=Poppins:wght@300&display=swap');

body{
  background-color: #F8F8F8;
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: Montserrat,Helvetica,Arial,serif;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.45;
  color: #6e6b7b;
}
</style>
