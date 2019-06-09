<template>
  <div id="app">
    <Quote :theQuote="something" />
    <CategoryButton quoteCategory='Courage' @clicked="onClickChild"></CategoryButton>
    <CategoryButton quoteCategory='Productivity' @clicked="onClickChild"></CategoryButton>
    <br/><br/><br/>
    <p style='position: fixed; bottom: 20px'>All quotes belong to their respective authors</p>
  </div>
</template>

<script>
import Quote from './components/Quote.vue'
import CategoryButton from './components/CategoryButton.vue'

var stronkQuotes = ["Over prepare then go with the flow",
"I assess the power of a will by how much resistance, pain, torture it endures and knows how to turn to its advantage",
"The individual has always had to struggle to keep from being overwhelmed by the tribe. If you try it, you will be lonely often, and sometimes frightened. But no price is too high to pay for the privilege of owning yourself",
"It is my ambition to say in ten sentences what others say in a whole book",
"The demand to be loved is the greatest of all arrogant presumptions",
"The doer alone learneth",
"We have art in order not to die of the truth",
"Glance into the world just as time were gone: and everything crooked will become straight to you",
"All things are subject to interpretation whichever interpretation prevails at a given time is a function of power and not truth",
"You have your way. I have my way. As for the right way, the correct way, and the only way, it does not exist",
"Emotion, which is suffering, ceases to be suffering as soon as we form a clear and precise picture of it",
"Don’t wait til your deathbed to tell people how you feel. Tell them to fuck off now",
"A splendid parade of death and uncertainty",
"A kiss is a lovely trick designed by nature to stop speech when words become superfluous",
"Love is spending the rest of your life with someone you want to kill and not doing it because you’d miss them"];

var shownQuote = 'Press buttons';

export default {
  data: function() {
    return{
      something: shownQuote
      }
    },
  name: 'app',
  components: {
    Quote,
    CategoryButton
  },
  methods: {
    onClickChild (value) {
      console.log(value);
      var bamboozle=parseInt(Math.random()*1000);
      if(value=='Courage'){
        this.something = stronkQuotes[bamboozle%10+5];
        console.log(bamboozle%10+6);
      }
      else if (value == 'Productivity'){
        this.something = stronkQuotes[bamboozle%5];
        console.log(bamboozle%6);
      }
      else {
        console.log('Error on button events')
      }
    }
  }
}
</script>

<style>
body{
  color: #023568;
  background-color: gray;
}

#app {
  padding: 2%;
  font-family: monospace;
  padding:5%;
  min-width:90%;
  text-align: center;
  position: absolute;
  top: 40%;
  margin-top: -37.5px; /* account for padding and border if not using box-sizing: border-box; */
}

h1{
  min-height: 65px;
}

button{
  color: #023568;
  min-width:20%;
  font-family: monospace;
  font-weight: bold;
  font-size: 18px;
  margin:20px;
  padding:20px;
  padding-top: 5px;
  padding-bottom: 5px;
}
</style>
