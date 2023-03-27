<template>
  <candy
    v-for="item in newfood"
    :name="item.name"
    :price="item.price"
    :img="item.img"
  ></candy>
</template>

<script>
import candy from "../components/tastyCards.vue";
export default {
  components: { candy },
  data() {
    return {
      newfood: [
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
          img: "data:image/jpeg;base64,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",
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
    };
  },
};
</script>

<style scoped></style>
