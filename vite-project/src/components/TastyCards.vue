<template>
  <ul>
    <li v-for="newfood in newfood">
      {{ newfood.name }} - ${{ newfood.price }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      newfood: [
        {
          id: 1,
          name: "Hersheys Organic Milk Chocolate Candy",
          img: (src =
            "https://www.cvs.com/bizcontent/merchandising/productimages/large/34000002405.jpg"),
          price: 3,
        },
        {
          id: 2,
          name: "Reeses Peanut Butter Cups",
          img: (src =
            "https://target.scene7.com/is/image/Target/GUEST_8a132d8b-a949-4592-89b1-af94e567055e?wid=488&hei=488&fmt=pjpeg"),
          price: 2,
        },
        {
          id: 3,
          name: "Skittles",
          img: (src =
            "https://assets.wakefern.com/is/image/wakefern/4000000160-001?$Mi9Product_detail$"),
          price: 1,
        },
        {
          id: 4,
          name: "Jolly Rancher Hard Candy, Assorted",
          img: (src =
            "https://shop.hersheys.com/on/demandware.static/-/Sites-master-us/default/dwcb23940b/images/hi-res/hsy-556868_1.png"),
          price: 10,
        },
        {
          id: 5,
          name: "Haribo GoldBears",
          img: (src =
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.haribo.com%2Fen-us%2Fproducts%2Fgoldbears&psig=AOvVaw1Z7sOQevPgWXkHNTuD8Jda&ust=1678889127310000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCLiT6cHL2_0CFQAAAAAdAAAAABAE"),
          price: 3,
        },
        {
          id: 6,
          name: "Airheads",
          img: (src =
            "https://economycandy.com/wp-content/uploads/2022/05/52b019dd-4765-41a4-852b-391d94f61d70.jpeg"),
          price: 5,
        },
        {
          id: 7,
          name: "Sour Patch Kids",
          img: (src =
            "https://i5.walmartimages.com/asr/d38f3189-dd80-4bf2-98fe-3254df18d171.b818170764ffd27c85df5017c72fdacd.jpeg"),
          price: 5,
        },
        {
          id: 8,
          name: "Kitkats",
          img: (src =
            "https://target.scene7.com/is/image/Target/GUEST_319372ae-60f5-4054-9394-59a2080c789e"),
          price: 5,
        },
        {
          id: 9,
          name: "Trolli Sour Brite Crawlers Gummi Worms",
          img: (src =
            "https://m.media-amazon.com/images/W/IMAGERENDERING_521856-T1/images/I/91ZgbCjCeXL.jpg"),
          price: 2,
        },
        {
          id: 10,
          name: "Sour Power Straws",
          img: (src =
            "https://cdn.shopify.com/s/files/1/0204/1514/products/SourPowerStrawsStrawberry_512x484.png?v=1655489971"),
          price: 1,
        },
      ],
    };
  },
};
</script>

<style scoped></style>
