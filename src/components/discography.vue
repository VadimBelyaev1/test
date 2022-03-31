<template>
  <section class="discography">
    <div class="line">
      <div class="music">
        <h3>NEVERMIND</h3>
      </div>
      <div class="music">
        <h3>INCESTICIDE</h3>
      </div>
      <div class="music">
        <h3>BLEACH</h3>
      </div>
    </div>
    <div class="line1">
      <div class="cover">
        <img src="../assets/nevermind.png" />
      </div>
      <div class="cover">
        <img src="../assets/Incesticide.png" />
      </div>
      <div class="cover">
        <img src="../assets/bleach.png" />
      </div>
    </div>
    <div class="line2">
      <div class="tracks">
        <p>
          1. Smells Like Teen Spirit<br />
          2. In Bloom<br />
          3. Come as You Are<br />
          4. Breed<br />
          5. Lithium<br />
          6. Polly<br />
          7. Territorial Pissings<br />
          8. Drain You<br />
          9. Lounge Act<br />
          10. Stay Away<br />
          11. On a Plain<br />
          12. Something in the way<br />
          13. Endless, Nameless<br />
        </p>
      </div>
      <div class="tracks1">
        <p>
          1. Serve the Servants<br />
          2. Scentless Apprentice<br />
          3. Heart-Shaped Box<br />
          4. Rape Me<br />
          5. Frances Farmer Will Have <br />
          Her Revenge on Seattle<br />
          6. Dumb<br />
          7. Very Ape<br />
          8. Milk It<br />
          9. Pennyroyal Tea<br />
          10. Radio Friendly Unit Shifter<br />
          11. Tourette's<br />
          12. All Apologies<br />
          13. Gallons of Rubbing Alcohol<br />
          Flow Through the Stri<br />
        </p>
      </div>
      <div class="tracks">
        <p>
          1. Blew<br />
          2. Floyd The Barber<br />
          3. About A Girl<br />
          4. School<br />
          5. Love Buzz<br />
          6. Paper Cuts<br />
          7. Negative Creep<br />
          8. Scoff<br />
          9. Swap Meet<br />
          10. Mr. Moustache<br />
          11. Sifting<br />
          12. Big Cheese<br />
          13. Downer<br />
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "discography",
};
</script>

<style lang="scss" scoped>
.discography {
  background: #f6d891;
  margin: 0;
}

.discography .line {
  display: flex;
  justify-content: space-between;
  margin-left: 150px;
  margin-right: 172px;
}

.discography .line1 {
  display: flex;
  justify-content: space-between;
  margin-left: 130px;
  margin-right: 130px;
}

.discography .line1 img {
  height: 154px;
  width: 154px;
}

.discography .line2 {
  display: flex;
  justify-content: space-between;
  margin-left: 96px;
  margin-right: 100px;
}

.discography .line2 .tracks {
  margin-top: 24px;
}

.discography .line2 .tracks1 {
  margin: 24px 0 29px 0;
}

.discography .line2 p {
  font-size: 18px;
}
</style>