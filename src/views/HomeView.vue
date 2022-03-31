<template>
  <div class="home">
    <section class="photo">
      <div class="kurt"></div>
    </section>
    <section class="info">
      <div class="head">
        <h2>ПЕВЕЦ. МУЗЫКАНТ. ПОЭТ. ХУДОЖНИК</h2>
      </div>
      <div class="group">
        <img src="../assets/group.png" />
      </div>
      <div class="menu">
        <a href="bio">БИОГРАФИЯ</a>
        <a href="disck">ДИСКОГРАФИЯ</a>
        <a href="tickets">БИЛЕТЫ</a>
        <a href="clips">КЛИПЫ</a>
      </div>
    </section>
    <section class="last">
      <div class="gitar"></div>
    </section>
    <section class="biography">
      <div class="selfie">
        <img src="../assets/kurt_solo.png" />
      </div>
      <div class="history">
        <p>
          Курт Кобейн (1967 – 1994) – певец, рок-музыкант, гитарист. Биография
          Курта Кобейна наиболее известна как история вокалиста группы «Нирвана»
          (Nirvana).<br />
          <br />
          Родился 20 февраля 1967 года в городе Абердин, штат Вашингтон. <br />
          Мелодичные рок-песни, исполняемые Куртом в составе группы «Нирвана»,
          соединили стили панк и поп. Группе удалось продать миллионы альбомов в
          начале 1990-х. Их песня «Smells Like Teen Spirit» стала настоящим
          гимном в 1991 году, долгое время продержавшись на вершине хит-парадов.
          Песня также помогла грандж-року повысить свои позиции относительно
          поп-музыки Майкла Джексона. Можно сказать, что после этого Сиэтл,
          находящийся неподалеку от города Абердин (где родился Кобейн), был
          нанесен на музыкальную карту Америки.<br />
          <br />
          Затем в биографии Курта Кобейна были выпущены такие альбомы, как
          «Bleach» (1989), «Nevermind» (1991), «In Utero» (1993). Некоторое
          время «Нирвана» была самой горячей группой в мире. Однако слава
          доставляла Курту неудобства, была его искусителем. Вскоре в жизни
          Кобейна возникла проблема с наркотиками. Он закрепил за собой статус
          рок-легенды, когда совершил самоубийство в 1994 году, выстрелив себе в
          рот.<br />
          Дополнительные данные: Кобейн в 1992 году женился на актрисе,
          рок-музыкантке Кортни Лав. В 1992 родилась дочь Курта Кобейна, Фрэнсис
          Бин.<br />
          Некоторые поклонники певца продолжают верить, что его убили. Однако
          возле тела Курта была найдена посмертная записка. Следователь по
          убийству установил, что певец сам нанес себе раны. Все же остаются
          фанаты, продолжающие утверждать, что смерть Кобейна подстроена,
          некоторые же обвиняют Кортни Лав в смерти Кобейна. Слухи были широко
          распространены, однако никем не проверялись. В 1998 году вышел фильм
          «Kurt and Courtney», рассказывающий биографию Курта Кобейна, а также
          его взаимоотношения с Кортни Лав, историю смерти Курта.<br />
        </p>
      </div>
    </section>
    <section class="poloska">
      <div class="line"></div>
    </section>
    <discography></discography>
    <section class="poloska">
      <div class="line"></div>
    </section>
    <tickets></tickets>
    <section class="poloska">
      <div class="line"></div>
    </section>
    <section class="clips">
      <div class="slts">
        <div class="video">
          <iframe
            width="1920"
            height="1080"
            src="https://www.youtube.com/embed/hTWKbfoikeg"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </section>
    <section class="poloska">
      <div class="line">
        <p>MADE BY <span>BELYAEV VADIM </span></p>
      </div>
    </section>
  </div>
</template>


<script>
// @ is an alias to /src
import discography from "../components/discography";
import tickets from "../components/tickets";

export default {
  name: "HomeView",
  components: {
    discography,
    tickets,
  },
};
</script>


<style lang="scss">
.photo {
  background: url("../assets/kurt4.png");
  background-repeat: no-repeat;
}

.photo .kurt {
  padding: 200px 0 0 0;
  height: 564px;
}

.info {
  padding: 22px 0;
  background-color: black;
}

.info .head {
  margin-bottom: 37px;
  text-align: center;
}

.info .head h2 {
  margin: 0;
  font-size: 72px;
  color: #f6d891;
  text-transform: uppercase;
}

.info .group {
  text-align: center;
}

.info .group img {
  margin: 37px 0 80px;
  height: 381px;
  width: 869px;
  justify-content: center;
}

.info .menu {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.info .menu a {
  margin: 0 50px 65px 49px;
  text-align: center;
  font-size: 26px;
  width: 189px;
  color: black;
  text-decoration: none;
  user-select: none;
  background: white;
  padding: 0.7em 1.5em;
}

.info .menu a:hover {
  background: #bbbbbb;
}

.last {
  background: url("../assets/kurt5.png");
  background-repeat: no-repeat;
}

.last .gitar {
  padding: 200px 0 0 0;
}

.biography {
  background: #f6d891;
  margin: 0;
  display: flex;
  align-items: center;
}

.biography .selfie img {
  width: 416px;
  height: 494px;
  margin-bottom: -4px;
  margin-right: 26px;
  padding-top: 84px;
}

.biography .history p {
  padding-bottom: 74px;
  font-size: 20px;
  margin-top: 37px;
  margin-right: 45px;
  display: inline-flex;
}

.poloska {
  background-color: black;
  height: 35px;
}

.clips {
  margin: 0;
  padding: 0;
}

.clips .slts {
  width: 100%;
  margin-left: auto;
  left: auto;
  right: auto;
}

.clips .slts .video {
  position: relative;
  padding-bottom: 56.25%;
  height: 0;
  overflow: hidden;
}

.poloska {
  margin: 0 auto;
  color: white;
}

.poloska p {
  padding: 0;
  text-align: center;
}

.poloska p span {
  color: red;
}
</style>