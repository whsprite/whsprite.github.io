<template>
  <div class="app-container">
    <Header></Header>
    <img id="top" class="img-1" src="https://raw.githubusercontent.com/whsprite/img/main/VCG211296241886.4435ht8s74k0.jpg" alt="" />
    <my-button @click="handleForm"></my-button>   
    <QA :qa="qa"></QA>
    <Card v-for="item in context" v-bind:key="item.title" :title="item.title" :text="item.text" :t="item.t"></Card>
    <ToTop></ToTop>
    <Footer>123</Footer>
    <Layer></Layer>
    <FormLayer v-show="on" @close="handleClose"></FormLayer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";
import Footer from "./components/Footer.vue";
import ToTop from "./components/ToTop.vue";
import QA from "./components/QA.vue";
import Layer from "./components/MyLayer.vue";
import FormLayer from "./components/FormLayer.vue";
import MyButton from "./components/MyButton.vue"
export default {
  data() {
    return {
      qa: {
        title: "よくある質問",
        t: "Q&A",
        text: [
          {
            q: "※ギルドの目標は何ですか？",
            a: "tiktokでライブを始めようとしている皆さんが、力を合わせて学び合い、一緒に進んでいくことを願って、ギルドを立ち上げました。",
          },
          {
            q: "※ギルドへの参加費はかかりますか",
            a: "ギルドでは、料金は一切かかりませんので、お気軽にご参加ください。",
          },
        ],
      },
      context: [
        {
          title: "About Us",
          text: "tiktokは9月にギルド機能をリリースを伴い、ライバー同士のコミュニケーションやコラボレーションを可能にし、より早くフォロワーを増やすために、このギルドを作りました。本ギルドはtiktokライブストリーミングチームの経験を生かして個人IPのインキュベーションに豊富な経験を持ち、健全と成熟のKOL育成システムを有します。tiktokと公式にパートナーシップも結んでおり、ストリームでの優先順位を上げさせ、露出を増やすことができる、トップKOLへの道を全力でサポートします！",
          t: "GUILD",
        },
      ],
      on: false,
    };
  },
  methods: {
    handleForm() {
      this.on = true;
    },
    handleClose(){
      this.on = false;
    }
  },
  components: {
    Header,
    Card,
    Footer,
    ToTop,
    QA,
    Layer,
    FormLayer,
    MyButton,
  },
};
</script>

<style scoped>
.app-container {
  min-height: 100%;
  position: relative;
  text-align: center;
  background-color: rgb(255, 255, 255);
}
.img-1 {
  width: 100%;
  z-index: -1;
}
</style>>

