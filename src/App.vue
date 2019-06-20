<template>
  <!-- <div id="app">
    <img width="25%" src="./assets/logo.png">
    <HelloWorld msg="Hello Vue in CodeSandbox!" />
  </div>-->
  <div id="app" class="columns">
    <div class="column">
      <TweetComponent v-for="tweet in tweets" :tweet="tweet"/>
    </div>
  </div>
</template>

<script>
import TweetComponent from "./components/TweetComponent";
const tweets = [
  {
    id: 1,
    name: "James",
    handle: "@jokerjames",
    img: "https://semantic-ui.com/images/avatar2/large/matthew.png",
    tweet: "If you don't succeed, dust yourself off and try again.",
    likes: 10
  },
  {
    id: 2,
    name: "Fatima",
    handle: "@fantasticfatima",
    img: "https://semantic-ui.com/images/avatar2/large/molly.png",
    tweet: "Better late than never but never late is better.",
    likes: 12
  },
  {
    id: 3,
    name: "Xin",
    handle: "@xeroxin",
    img: "https://semantic-ui.com/images/avatar2/large/elyse.png",
    tweet: "Beauty in the struggle, ugliness in the success.",
    likes: 18
  }
];

export default {
  name: "App",
  components: {
    TweetComponent
  },
  data() {
    return {
      tweets
    };
  }
};
</script>

<style scoped>
#app {
  height: 100%;
  padding-top: 0px;
  text-align: center;
}

#app .button {
  margin-bottom: 20px;
}

#app .tweet {
  max-width: 500px;
  margin: 0 auto;
  padding-bottom: 15px;
}

#app .box {
  margin-bottom: 0;
  border-radius: 0;
}

#app .content small {
  color: #00d1b2;
}

#app img {
  border-radius: 30px;
}

#app .level-item {
  padding-left: 10px;
  color: #00d1b2;
}

#app input:focus {
  border-color: #00d1b2;
}

#app .likes {
  padding: 0 7.5px;
}

#app input {
  font-weight: bold;
}

#app .tweets-move {
  transition: transform 1s;
}
</style>
