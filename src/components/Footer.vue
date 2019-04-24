<template>
  <div class="footer flex-center">
    <div class="main container">
      <section class="section-left">
        <h5>About Me</h5>
        <p>We have tested a number of registry fix and clean utilities and present our top 3 list on our site for your convenience.</p>
        <p>Copyright ©2019 All rights reserved</p>
      </section>
      <section class="section-right">
        <h5>Newsletter</h5>
        <p>Stay updated with our latest trends</p>
        <form>
          <input type="email" id="email" name="email" value="Enter Email Address">
          <input type="submit" value="➤" id="submit">
        </form>
      </section>
    </div>
  </div>
</template>

<script>
export default { name: "Footer" };
</script>

<style scoped>
.footer {
  background-color: #04091e;
  color: #fff;
}

.main {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  flex-wrap: wrap;
}

section {
  max-width: 500px;
  min-width: 150px;
  padding: 20px 10px;
}

#email {
  font-family: "Segoe UI", sans-serif;
  color: #777;
  min-width: 190px;
  height: 35px;
  box-sizing: border-box;
}

#submit {
  font-family: "Segoe UI", sans-serif;
  color: #fff;
  background-color: #8490ff;
  border: none;
  height: 35px;
  box-sizing: border-box;
}

@media (max-width: 830px) {
  .main {
    justify-content: center;
    flex-direction: column;
    text-align: center;
  }

  section {
    max-width: none;
  }
}
</style>
