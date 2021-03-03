<template>
  <div class="wrap">
    <Navbar title="Eesti Kott"/>
    <div class="image"></div>
    <div class="container">
      <Header title="Kuidas on eesti keeles?"/>
      <QA question="Hello"/>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header"
import Navbar from "./components/Navbar"
import QA from "./components/QA"

export default {
  name: 'App',
  components: {
    Header,
    Navbar,
    QA
  },
  data() {
    return {
      json_data: []
    }
  },
  created() {
    this.json_data = [
      {
        id: 1,
        eng: "How are you?",
        ee: "Kuidus läheb?",
        did_learn: 0
      },
      {
        id: 2,
        eng: "Thank you.",
        ee: "Aitäh",
        did_learn: 1
      }
    ]
  }
}
</script>

<style>
  .wrap {
    position: relative;
    height: 100%;
  }
  .container {
    max-width: 300px;  
    margin: 0;
    overflow: auto;
    min-height: 300px;
    padding: 30px;
    border-radius: 5px;
    background-color: rgba(255, 255, 255, 0.3);
    position: absolute;
    top: 300%;
    left: 10%;
  }
  .image {
    height: 900px;
    width: 100%;
    position: absolute;
    top: 0;
    z-index: -1; 
    background-image: url("./assets/Moose_Kalle_Pihelgas_cropped.jpg");
    background-repeat: no-repeat;
    background-position: center center;
    background-attachment: fixed;
  }

</style>
