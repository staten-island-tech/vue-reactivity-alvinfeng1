<template>
  <candy
    v-for="item in food"
    :name="item.name"
    :price="item.price"
    :img="item.img"
  ></candy>
</template>

<script>
import candy from "../components/TasTyCards.vue";
export default {
  components: { candy},
  data() {
    return {
      food: [
        {
          id: 1,
          name: "Hersheys Organic Milk Chocolate Candy",
          img: "https://www.cvs.com/bizcontent/merchandising/productimages/large/34000002405.jpg",
          price: 3,
        },
        {
          id: 2,
          name: "Reeses Peanut Butter Cups",
          img: "https://target.scene7.com/is/image/Target/GUEST_8a132d8b-a949-4592-89b1-af94e567055e?wid=488&hei=488&fmt=pjpeg",
          price: 2,
        },
        {
          id: 3,
          name: "Skittles",
          img: "https://assets.wakefern.com/is/image/wakefern/4000000160-001?$Mi9Product_detail$",
          price: 1,
        },
        {
          id: 4,
          name: "Jolly Rancher Hard Candy, Assorted",
          img: "https://shop.hersheys.com/on/demandware.static/-/Sites-master-us/default/dwcb23940b/images/hi-res/hsy-556868_1.png",
          price: 10,
        },
        {
          id: 5,
          name: "Haribo GoldBears",
          img: "https://assets.haribo.com/image/upload/s--q8QScoFX--/ar_2700:3661,c_fill,f_auto,q_60/w_763/v1/consumer-sites/international/Goldbears.png",
          price: 3,
        },
        {
          id: 6,
          name: "Airheads",
          img: "https://economycandy.com/wp-content/uploads/2022/05/52b019dd-4765-41a4-852b-391d94f61d70.jpeg",
          price: 5,
        },
        {
          id: 7,
          name: "Sour Patch Kids",
          img: "https://i5.walmartimages.com/asr/d38f3189-dd80-4bf2-98fe-3254df18d171.b818170764ffd27c85df5017c72fdacd.jpeg",
          price: 5,
        },
        {
          id: 8,
          name: "Kitkats",
          img: "https://target.scene7.com/is/image/Target/GUEST_319372ae-60f5-4054-9394-59a2080c789e",
          price: 5,
        },
        {
          id: 9,
          name: "Trolli Sour Brite Crawlers Gummi Worms",
          img: "https://m.media-amazon.com/images/W/IMAGERENDERING_521856-T1/images/I/91ZgbCjCeXL.jpg",
          price: 2,
        },
        {
          id: 10,
          name: "Sour Power Straws",
          img: "https://cdn.shopify.com/s/files/1/0204/1514/products/SourPowerStrawsStrawberry_512x484.png?v=1655489971",
          price: 1,
        },
        {
          id: 11,
          name: "Kinder Surprise",
          img: "https://www.kinder.com/uk/sites/kinder_uk/files/2019-11/chocolate-egg-kinder-surprise-uk.png?t=1679492331",
          price: 3,
        },
        {
          id: 12,
          name: "TWIZZLERS PULL 'N' PEEL Cherry Flavored Laydown Bag",
          img: "https://m.media-amazon.com/images/I/71Q5yTQJCOS._SX679_.jpg",
          price: 1,
        },
        {
          id: 13,
          name: "Hi-Chew Sensationally Chewy Japanese Fruit Candy, Acai",
          img: "https://m.media-amazon.com/images/I/71uhe6xCl8L._SX679_.jpg",
          price: 2,
        },
        {
          id: 14,
          name: "Glico Caplico Sakura Mini Ice Cream Snacks - 10 pcs",
          img: "https://cdn.shopify.com/s/files/1/0713/9790/0584/products/20230317_005_900x.jpg?v=1679030937",
          price: 10,
        },
        {
          id: 15,
          name: "Coris Whistle Candy - Grape",
          img: "https://cdn.shopify.com/s/files/1/0713/9790/0584/products/20200311_013_900x.jpg?v=1675384170",
          price: 3,
        },
      ],
      cart:[]
    };
  },
};
</script>

<style scoped></style>
