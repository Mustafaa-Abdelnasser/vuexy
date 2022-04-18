<template>
  <div class="products-container">
    <div class="products-head">
      <h6>{{filteredItems.length}} results found</h6>
      <div class="f-btn">
        <button class="feat" @click="toggle">
          <h1>{{filteredValue}}</h1>
          <i class="fa-solid arrw fa-angle-down"></i>
          <ul class="featured-menu star-menu dNone" id="featured" >
                                <li class="hov featured-item" @click="featured"><span>Featured</span></li>
                                <li class="hov featured-item" @click="ascending"><span>Lowest</span></li>
                                <li class="hov featured-item" @click="descending"><span>Highest</span></li>
                        </ul>
        </button>
        <button class="grid" ><i class="fa-solid fa-border-all"></i></button>
        <button class="list" ><i class="fa-solid fa-list"></i></button>
      </div>
    </div>

    <div class="s-input">
      <input type="search" placeholder="search product" v-model="search" >
      <i class="fa-solid lens fa-magnifying-glass"></i>
    </div>

    <div class="prod">
      <div v-for="item in filteredItems " :key="item.id" class="crd">
        <div class="crd-img">
            <img :src= " item.img " alt="">
        </div>
        <div class="crd-body">
          <div class="crd-wrapper">
            <div class="crd-rating">
              <ul class="str-rate">
                <li><i class="icon fa-solid orange fa-star light light"></i></li>
                <li><i class="icon fa-solid orange fa-star light light"></i></li>
                <li><i class="icon fa-solid orange fa-star light light"></i></li>
                <li><i class="icon fa-solid orange fa-star light light"></i></li>
                <li><i class="icon fa-regular fa-star light light"></i></li>
              </ul>
            </div>
            <div class="it-price">
              <h6>{{item.price}}</h6>
            </div>
          </div>
          <a class="it-name" href="#"><h6>{{item.name}}</h6></a>
          <p class="it-dsc">
            {{item.discription}}
          </p>
        </div>
        <div class="crd-opt">
          <a class="wsh" href=""
            ><i class="icon fa-regular fa-heart"></i>Wishlist</a
          >
          <a class="crt-icon" href=""
            ><i class="icon fa-solid fa-cart-shopping"></i>View In Cart</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props : ['items'],
  data(){
    return{
      search: "",
      srch : "",
      filtered : this.items,
      filteredValue: ''
    }
    
  },
  computed: {
    filteredItems(){
      this.srch=this.search.charAt(0).toUpperCase() + this.search.slice(1);
      this.filtered = this.items.filter(item => item.name.includes(this.srch));
      this.filteredValue = "Featured";
      return this.filtered
    },
    ascending(){
      this.filtered = this.filtered.sort((a, b ) =>  a.price - b.price);
      this.filteredValue = "Lowest";
      return this.filtered
    },
    descending(){
      this.filtered = this.filtered.sort((a, b ) =>  b.price - a.price);
      this.filteredValue = "Highest";
      return this.filtered
    },
    featured(){
      this.filtered = this.items.filter(item => item.name.includes(this.srch));
      this.filteredValue = "Featured";
      return this.filtered
    }
  },
  methods: {
    toggle: function(event){
      document.getElementById("featured").classList.toggle("dNone")
    }
  }
};
</script>

<style>
.prod {
  width: 915.2px;
  margin-top: 28px;
  display: flex;
  /* justify-content: space-between; */
  flex-flow: wrap;
}
.featured-menu{
    width: 138px; 
    height: 115.5px;
    margin: 0;
    padding: 7px 0;
    top: 44px;
    left: -19px;
    z-index: 111;
}
.featured-menu .featured-item {
  display: flex;
  font-family: Montserrat,Helvetica,Arial,serif;
  width: 102.2px;
  height: 20.3px;
  padding: 9.1px 17.92px ;
  font-weight: 400;
  color: #6e6b7be8;
  white-space: nowrap;
  font-size: 14px;
  justify-content: flex-start;
}
.crd {
  min-width: 286.4px;
  height: 366px;
  margin : 0 9px  ;
  margin-bottom: 28px;
  overflow: hidden;
  box-shadow: 0 4px 24px 0 rgb(34 41 47 / 10%);
  background-color: #fff;
  border-radius: 0.428rem;
  flex-direction: column;
  display: flex;
  transition: 0.3s ease-in-out;
}
.crd:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 25px 0 rgb(34 41 47 / 25%);
}
.crd-img {
  align-items: center;
  width: 286.4px;
  height: 214.56px;
  padding-top: 7px;
}
.crd-img img{
    width: 100%;
    height: 100%;
}
.crd-body {
  box-sizing: border-box;
  width: 286.4px;
  height: 104.5px;
  padding: 14px;
  letter-spacing: 0.14px;
  line-height: 20.3px;
  font-weight: 400;
  font-size: 14px;
}

.crd-wrapper {
  width: 258.4px;
  height: 25.4px;
  display: flex;
  justify-content: space-between;
  margin: 0px;
}

.crd-rating {
  width: 94px;
  height: 20.3px;
  font-size: 14px;
}
.str-rate {
  list-style: none;
  display: flex;
  font-size: 14px;
  margin: 0px;
  padding: 0px;
}
.str-rate .icon {
  font-size: 14px;
  width: 16px;
  height: 16px;
  padding: 0px;
}

.it-price h6 {
  padding: 0px;
  margin: 0px;
  font-size: 14px;
  font-family: inherit;
  line-height: 1.2;
  font-weight: 600;
}
.it-name {
  text-decoration: none;
  width: 258.4px;
  height: 16.8px;
}
.it-name h6 {
  margin: 0px;
  text-decoration: none;
  color: #6e6b7b;
  font-size: 14px;
  font-weight: 600;
  line-height: 1.2;
  font-family: inherit;
  margin-top: 10px;
  letter-spacing: 0.4px;
}
.it-dsc {
  box-sizing: border-box;
  width: 258.4px;
  height: 21px;
  margin-top: 2.8px;
  font-size: 12.25px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  color: #6e6b7b;
}
.crd-opt {
  width: 286.42px;
  height: 39.6px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  cursor: pointer;
}

.crd-opt .wsh {
  box-sizing: border-box;
  display: flex;
  width: 126.93px;
  height: 40px;
  text-align: center;
  text-decoration: none;
  padding: 0.786rem 1.5rem;
  letter-spacing: 0.4px;
  color: #2a2e30;
  font-size: 14px;
  line-height: 1;
  background-color: #f6f6f6;
}
.crd-opt .wsh:hover {
  background-color: #e3e3e3;
}
.crd-opt .icon {
  width: 14px;
  height: 14px;
  margin-right: 7px;
  padding: 0px;
}
.light{
    color: rgb(185, 185, 195);
}

.crd-opt .crt-icon {
  box-sizing: border-box;
  width: 159.49px;
  /* height: 39.6px; */
  text-align: center;
  text-decoration: none;
  padding: 0.786rem 1.5rem;
  letter-spacing: 0.4px;
  color: #2a2e30;
  font-size: 14px;
  line-height: 1;
  background-color: #7367f0;
  color: #ffff;
}
.crd-opt .crt-icon:hover {
  box-shadow: 0 8px 25px -8px #7367f0;
}
.products-container {
    position: absolute;
  width: 915.2px;
  height: 1356.2px;
  margin-left: 576px;
  float: right;
  margin-top: 172.9px;
  padding-right: 28px;
  
}
.products-head {
  display: flex;
  height: 20px;
  align-items: center;
  justify-content: space-between;
}
.products-head h6 {
  margin: 0;
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 0.8px;
}
.f-btn {
  justify-content: flex-end;
  align-items: flex-end;
}
.f-btn .feat {
  background-color: #f8f8f8;
  padding: 11px 16px;
  border: 1px solid rgb(115, 103, 240);
  border-radius: 5px;
  cursor: pointer;
  width: 123px;
  height: 38px;
}
.arrw {
  color: #7367f0;
  padding-left: 10px;
}
.f-btn button h1 {
  color: #7367f0;
  font-size: 14px;
  line-height: 1;
  font-weight: 500;
  letter-spacing: 0.7px;
  margin: 0;
  padding: 0;
  display: inline;
}

.f-btn .feat:hover {
  background-color: rgba(115, 103, 240, 0.04);
}
.feat {
  position: relative;
  margin-right: 14px;
}
.grid,
.list {
  width: 47px;
  height: 38px;
  padding: 6.8px 14px;
  color: #7367f0;
  background-color: #f8f8f8;
  border: 1px solid rgb(115, 103, 240);
  cursor: pointer;
  font-size: 15px;
}
.grid {
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  background-color: #7367f033;
}
.list {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}
.list:hover {
  background-color: rgba(115, 103, 240, 0.04);
}
.s-input {
  display: flex;
  padding-top: 6.132px;
  align-items: center;
  justify-content: space-between;
  width: 100%;
      margin-top: 22px;
  background-color: rgb(255, 255, 255);
  height: 48px;
  border-radius: 5px;
  box-shadow: 0 2px 8px 0 rgb(34 41 47 / 14%);
}
.orange{
    color: #ff9f43;
}

.s-input input {
  width: 90%;
  height: 40px;
  color: #6e6b7b;
  padding: 0px 0px 6.132px 17.5px;
  border: none;
}
.lens{
    margin-right: 15px;
}
::-webkit-input-placeholder {
  color: #b9b9c3;
}
</style>