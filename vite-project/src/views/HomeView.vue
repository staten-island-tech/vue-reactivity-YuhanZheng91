<template>
  <div>
    <DestCard
      v-for="destination in destinations"
      :key="destination.name"
      :Destination="destination"
      @addToCart="addToCart"
    />
  </div>
</template>

<script setup>
import DestCard from "@/components/DestCard.vue";
const destinations = [
  {
    name: "One's Lost Gadget",
    desc: "A gadget without an owner. A strange, weird human-made gadget. Its purpose is unknown.",
    image: "https://tfipost.com/wp-content/uploads/2022/11/iPhone-15-back-view.jpg",
    imageDesc: "a gadget with a black surface",
    price: 1000000000,
  },
  {
    name: "Broken Egg Shells",
    desc: "Egg shells without much value. The shells belong to a baby dokkaebi who hatched years ago.",
    image: "http://cliparts.co/cliparts/8TE/6jR/8TE6jRXzc.png",
    imageDesc: "Yellow egg shells that are broken and cracked.",
    price: 9158,
  },
  {
    name: "Broken Faith",
    desc: "A sword with the former purpose of destroying the world. It broke in the process.",
    image: "https://i.pinimg.com/originals/ff/65/8f/ff658fe0d80dfebe9005b948e6bca040.jpg",
    imageDesc: "A bright double-edged sword with a silver hilt, welding the properties of divinity, dark, and fire.",
    price: 999999999,
  },
  {
    name: "Elf's Elixir",
    desc: "A potion that restores wounds.",
    image: "https://st2.depositphotos.com/1006187/7519/i/950/depositphotos_75194609-stock-photo-green-potion-in-the-bottle.jpg",
    imageDesc: "A round potion bottle containing light green liquid",
    price: 5000,
  },
  {
    name: "Artifically Flavored Lemon Lollipop",
    desc: "A lollipop meant for the purpose of eliminating exhaustion and restores alertness. The flavor is the best as well.",
    image: "https://img1.etsystatic.com/032/0/5779110/il_570xN.585315175_3v39.jpg",
    imageDesc: "A lollipop with yellow candy. Despite being artificially flavored, it tastes really good.",
    price: 5100,
  },
  {
    name: "Random Weapon Box",
    desc: "Want SSSS-grade weapons? Here it is! Buy one and get a random weapon with a great chance of getting a legendary weapon.",
    image: "",
    imageDesc: "A package thing with an icon of two swords.",
    price: 1500,
  },
  {
    name: "Random Skill Box",
    desc: "Want SSSS-grade skill? Here it is! Buy one and get a random skill with a great chance of getting a legendary skill.",
    image: "",
    imageDesc: "A package looking thing with an icon showing a thumbs-up",
    price: 1500,
  },
  {
    name: "Random Armor Box",
    desc: "Want SSSS-grade armor? Here it is! Buy one and get a random armor with a great chance of getting a legendary armor.",
    image: "",
    imageDesc: "A package looking thing with an icon of a helmet.",
    price: 1500,
  },
  {
    name: "Recovery Package",
    desc: "Recover from injury and fatigue!",
    image: "",
    imageDesc: "A package-looking thing with an icon showing a plus sign.",
    price: 1000,
  },
  {
    name: "Sword of Judgement",
    desc: "A sword used by the strongest woman loved by many. The judge of destruction shall return and reclaim what is hers.",
    image: "",
    imageDesc: "A longsword with a large red-colored eye between the hilt and blade. The blade is black with hints of red.",
    price: 1000000,
  },
  {
    name: "The Present",
    desc: "An abandoned, custom-made pocket watch. A reminder of the present to a dear regressor.",
    image: "",
    imageDesc: "A silver pocket watch with 'Aileen' carved on the bottom of it.",
    price: 5049,
  },
  {
    name: "Diary of Yuri di Aristel",
    desc: "A notebook belonging to a particular author, who wrote and waited more than 50 years for just that one reader. Where has he gone?",
    image: "",
    imageDesc: "A hardcover diary; it has a black leather cover and white pages. Each page is filled with a foreign language and a brilliant cursive.",
    price: 4951,
  },
];


</script>

<style scoped>

</style>