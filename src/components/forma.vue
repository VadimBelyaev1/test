<template>
  <div class="pokupka">
    <div class="foot">
      <div class="gorod">
        <p style="color: black">{{ city }}</p>
        <p5 style="color: black">{{ day }}</p5>
      </div>
      <div class="live">
        <p style="color: #f6d891">ПОКУПКА БИЛЕТОВ</p>
        <button class="button">LIVE BAND</button>
      </div>
    </div>
    <div class="buy">
      <div v-if="!isVisibleSucces">
        <!--<p style="color: white">{{ city }}</p>-->
        <div class="select">
          <p2> Выбор ряда: </p2>
          <select name="row_selection">
            <option selected></option>
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
            <option>5</option>
            <option>6</option>
            <option>7</option>
            <option>8</option>
            <option>9</option>
          </select>
          <p2> Выбор места: </p2>
          <select name="place">
            <option selected></option>
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
            <option>5</option>
            <option>6</option>
            <option>7</option>
            <option>8</option>
            <option>9</option>
            <option>10</option>
            <option>11</option>
            <option>12</option>
            <option>13</option>
            <option>14</option>
            <option>15</option>
            <option>16</option>
            <option>17</option>
            <option>18</option>
            <option>19</option>
            <option>20</option>
            <option>21</option>
            <option>22</option>
            <option>23</option>
            <option>24</option>
            <option>25</option>
            <option>26</option>
            <option>27</option>
            <option>28</option>
            <option>29</option>
            <option>30</option>
          </select>
        </div>
        <div class="table">
          <div class="hall">
            <img src="../assets/concert.png" />
          </div>
          <div class="space">
            <img src="../assets/micro.png" />
          </div>
          <div class="fio">
            <div class="char">
              <div class="field">
                <label> Ваше имя </label>
                <input type="text" />
              </div>

              <div class="field">
                <label> Ваша фамилия</label>
                <input type="text" />
              </div>

              <div class="field">
                <label> Введите email</label>
                <input type="email" />
              </div>

              <div class="field">
                <label> Введите номер телефона</label>
                <input
                  type="tel"
                  pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}"
                  required
                />
              </div>
            </div>
            <div class="force">
              <div class="summa">
                <p3>СУММА ПОКУПКИ: <br />2500</p3>
                <input
                  button
                  type="submit"
                  value="КУПИТЬ БИЛЕТ"
                  class="sub"
                  v-on:click="isVisibleSucces = true"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div v-if="isVisibleSucces" class="close"></div>
    <p v-on:click="doSomething" class="close">Закрыть</p>
  </div>
</template>

<script>
export default {
  name: "forma",
  props: ["city", "day"],

  data: function () {
    return {
      isVisibleSucces: false,
    };
  },
  methods: {
    doSomething() {
      this.$emit("updateParent", {
        close: true,
      });
    },
  },
};
</script>

<style scoped>
.pokupka {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: space-around;
  z-index: 11;
}

.foot {
  width: 1200px;
  height: 200px;
  margin-bottom: 562px;
  background-repeat: no-repeat;
  background-size: contain;
  background-image: url("../assets/head.png");
}
.foot .gorod p {
  margin: 23px 0 0 88px;
  text-transform: uppercase;
  font-size: 30px;
  line-height: 35px;
  z-index: 11;
}

.foot .gorod p5 {
  margin: 23px 0 0 123px;
  text-transform: uppercase;
  font-size: 30px;
  line-height: 35px;
}

.foot .live {
  display: flex;
  justify-content: flex-end;
  margin-right: 23px;
}

.foot .live p {
  margin: 10px 125px 0 560px;
  font-size: 40px;
  line-height: 46px;
}

.foot .live .button {
  font-family: Underdog;
  position: absolute;
  width: 59.94px;
  height: 60px;
  color: #fff;
  text-decoration: none;
  user-select: none;
  background: #d10202;
  padding: 0.5em 0.5em;
  border-radius: 4px;
  border: none;
}
.buy {
  position: fixed;
  width: 1200px;
  height: 400px;
  background-color: #f6d891;
}

.buy select {
  width: 124px;
  height: 17px;
  margin-top: 10px;
  border: 0;
  border-radius: 3px;
}
.pokupka .hall {
  margin: 10px 0 22px 34px;
}
.pokupka .hall img {
  margin-top: -100px;
  width: 500px;
  height: 344px;
}
.pokupka p2 {
  margin-left: 20px;
}

.pokupka .summa {
  font-size: 20px;
  margin-left: 40px;
  margin-top: 100px;
  display: flex;
  align-items: center;
  text-align: center;
}
.pokupka .table {
  display: flex;
  align-items: center;
}
.pokupka .table .space {
  margin-left: 10px;
  margin-bottom: 28px;
}

.pokupka .table .space img {
  margin-top: -100px;
  width: 175px;
  height: 320px;
}

.pokupka .table .fio {
  margin-left: 14px;
  text-transform: uppercase;
  margin-bottom: 200px;
}

.pokupka .table .fio .field {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
}
.pokupka .table .fio label {
  font-size: 15px;
  float: left;
  padding-right: 15px;
}

.pokupka .table .fio input {
  display: block;
}

.pokupka .table .summa input {
  margin-left: 50px;
}
.pokupka .fio .char .force {
  margin-top: 73px;
}

.pokupka .close {
  margin-top: 100px;
  display: flex;
  justify-content: center;
}
.pokupka p {
  font-size: 26px;
  display: flex;
  justify-content: flex-start;
}
.pokupka .sub {
  width: 125px;
  height: 50px;
  background-color: #d10202;
  color: #fff;
}
.pokupka input {
  position: relative;
  right: 0;
  border: 0;
  border-radius: 3px;
  display: block;
  margin-bottom: 15px;
  width: 157px;
  height: 15px;
}

.close {
  position: absolute;
  color: #fff;
  font-size: 30px;
  cursor: pointer;
  right: 30px;
  top: -75px;
}

.close .buy {
  background-color: black;
}
</style>