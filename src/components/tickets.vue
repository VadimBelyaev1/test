<template>
  <section class="tickets">
    <div class="city1">
      <div class="cities">
        <span class="city">КАЛИНИНГРАД</span><br />
        <p1 class="day">25.03.2023</p1>
      </div>
      <div class="buttons">
        <div class="liveband">
          <button class="liveband">LIVE<br />BAND</button>
        </div>
        <div class="buy_tickets">
          <button
            class="buy"
            v-on:click="
              isVisible = true;
              isData = 'Калининград';
              isDay = '25.03.2023';
            "
          >
            КУПИТЬ
          </button>
        </div>
      </div>
    </div>

    <div class="city2">
      <div class="cities">
        <span class="city">САНКТ-ПЕТЕРБУРГ</span><br />
        <p1 class="day">21.05.2023</p1>
      </div>
      <div class="buttons">
        <div class="liveband">
          <button class="liveband">LIVE<br />BAND</button>
        </div>
        <div class="buy_tickets">
          <button
            class="buy"
            v-on:click="
              isVisible = true;
              isData = 'САНКТ-ПЕТЕРБУРГ';
              isDay = '21.05.2023';
            "
          >
            КУПИТЬ
          </button>
        </div>
      </div>
    </div>
    <forma
      v-if="isVisible"
      :city="isData"
      :day="isDay"
      @updateParent="onUpdateSalary"
    ></forma>
  </section>
</template>

<script>
import forma from "./forma.vue";

export default {
  name: "tickets",
  components: {
    forma,
  },
  data: function () {
    return {
      isData: true,
      isVisible: false,
    };
  },
  methods: {
    onUpdateSalary(someData) {
      this.isVisible = !someData.close;
    },
  },
};
</script>

<style lang="scss" scoped>
.tickets {
  background: #f6d891;
  margin: 0;
}

.tickets p {
  position: fixed;
  top: 50px;
  right: 50px;
  color: #fff;
  font-size: 30px;
  cursor: pointer;
}

.tickets .cities {
  margin-left: 382px;
  padding-top: 16px;
  padding-bottom: 16px;
}

.tickets .city1 {
  display: flex;
  justify-content: space-around;
  align-items: baseline;
}

.tickets .city1 p1 {
  font-size: 12px;
}

.tickets .city1 .buy_tickets {
  margin-right: 415px;
  margin-left: 13px;
}

.tickets .city1 .buttons {
  margin-left: 355px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.tickets .city1 .liveband button {
  color: #fff;
  text-decoration: none;
  user-select: none;
  background: red;
  padding: 0.5em 0.5em;
  border-radius: 4px;
  border: none;
}

.tickets .city1 .buy_tickets button {
  cursor: pointer;
  font-size: 18px;
  color: #fff;
  text-decoration: none;
  user-select: none;
  background: black;
  padding: 0.6em 1.7em;
  border-radius: 4px;
  border: none;
}

.tickets .city2 {
  display: flex;
  justify-content: space-around;
  align-items: baseline;
}

.tickets .city2 p1 {
  font-size: 12px;
}

.tickets .city2 .buy_tickets {
  margin-right: 415px;
  margin-left: 13px;
}

.tickets .city2 .buttons {
  margin-left: 326px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.tickets .city2 .liveband button {
  color: #fff;
  text-decoration: none;
  user-select: none;
  background: red;
  padding: 0.5em 0.5em;
  border-radius: 4px;
  border: none;
}

.tickets .city2 .buy_tickets button {
  cursor: pointer;
  font-size: 18px;
  color: #fff;
  text-decoration: none;
  user-select: none;
  background: black;
  padding: 0.6em 1.7em;
  border-radius: 4px;
  border: none;
}
</style>