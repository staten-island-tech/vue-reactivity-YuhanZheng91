<template>
    <div>
        <h1>Dokkaebi Bag</h1>
        <h2>Items</h2>
        <div class="bigCont1">
        <div class="containerI">
        <div class="cardI" v-for="(item, index) in items" :key="index">
            <h2>{{ item.name }} - ${{ item.price }}</h2>
            <h3>{{ item.desc }}</h3>
            <button @click="addItemToCart(item)">Add to Cart</button>
        </div>
        </div>
        </div>
  
        <h2>Cart</h2>
        <div class="bigCont2">
        <div class="containerC">
        <div class="cardC" v-for="(cartItem, index) in cart" :key="index">
            <h2> {{ cartItem.name }} - ${{ cartItem.price }} </h2>
            <h3> {{ cartItem.desc }}</h3>
            <button @click="removeItemFromCart(index)">Remove</button>
        </div>
        </div>
    
        </div>
    </div>
    </template>
      
    <script>
    export default {
      data() {
        return {
          items: [
    {
      name: "One's Lost Gadget",
      desc: "A gadget without an owner. A strange, weird human-made gadget. Its purpose is unknown.",
      image: "",
      imageDesc: "a gadget with a black surface",
      price: 1000000000,
    },
    {
      name: "Broken Egg Shells",
      desc: "Egg shells without much value. The shells belong to a baby dokkaebi who hatched years ago.",
      image: "",
      imageDesc: "Yellow egg shells that are broken and cracked.",
      price: 9158,
    },
    {
      name: "Broken Faith",
      desc: "A sword with the former purpose of destroying the world. It broke in the process.",
      image: "",
      imageDesc: "A bright double-edged sword with a silver hilt, welding the properties of divinity, dark, and fire.",
      price: 999999999,
    },
    {
      name: "Elf's Elixir",
      desc: "A potion that restores wounds.",
      image: "",
      imageDesc: "A round potion bottle containing light green liquid",
      price: 5000,
    },
    {
      name: "Artifically Flavored Lemon Lollipop",
      desc: "A lollipop meant for the purpose of eliminating exhaustion and restores alertness. The flavor is the best as well.",
      image: "",
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
          ],
          cart: [],
        };
      },
      methods: {
        addItemToCart(item) {
          this.cart.push(item);
        },
        removeItemFromCart(index) {
          this.cart.splice(index, 1);
        },
      },
    };
    </script>
      
    <style scoped>
    body{
        background-color: #ffffff;

    }
    
    .cardI, .cardC{
        background-color: #808080;
        padding: 3%;
        margin: 1.5% auto;
        text-align: center;
        width: 30%;
        align-items: center;
    }
    
    .cardC{
        background-color: #373737;
        color: white;
    }
    .containerI, .containerC{
        display: flex;
        flex: 1;
        flex-wrap: wrap;
    }
    
    .containerC{
        flex: 1;
        background-color: #808080;
    }
    .containerI{
        flex: 2;
    }
    
    h1{
      text-align: center;
      
    }
    h2{
        font-weight: bold;
    }
    
    .bigCont1, .bigCont2{
      display: flex;
    }

    h3{
        font-size: 100%;
        font-weight: normal;
    }
    </style>