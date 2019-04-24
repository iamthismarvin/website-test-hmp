<template>
  <div class="feedback flex-center">
    <div class="main container">
      <h1 class="title">Client's Feedback About Me</h1>
      <p
        class="description"
      >It is very easy to start smoking but it is an uphill task to quit it. Ask any chain smoker or even a person.</p>
      <div class="quotes flex-row-around">
        <div
          class="quote flex-row-between"
          v-for="{id, name, title, message} in feedback"
          :key="id"
        >
          <div class="avatar-section flex-center">
            <img class="avatar" src="../images/image.svg" alt="avatar">
          </div>
          <div class="message-section">
            <p>{{message}}</p>
            <h2>{{name}}</h2>
            <p>{{title}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Feedback",
  data: () => ({
    feedback: [
      {
        id: 0,
        name: "Harriet Maxwell",
        title: "CEO at Google",
        message:
          "Do you want to be even more successful? Learn to love learning and growth. The more effort you put into improving your skills, the bigger the payoff you."
      },
      {
        id: 1,
        name: "Carolyn Craig",
        title: "CEO at Facebook",
        message:
          "A purpose is the eternal condition for success. Every former smoker can tell you just how hard it is to stop smoking cigarettes. However."
      }
    ]
  })
};
</script>

<style scoped>
.feedback {
  background-color: #f0f0f0;
}

.main {
  text-align: center;
}

.quotes {
  text-align: start;
  flex-wrap: wrap;
}

.quote {
  background-color: #fff;
  max-width: 550px;
  margin: 10px;
  padding-right: 20px;
}

.avatar-section {
  padding: 20px;
}

img.avatar {
  border-radius: 50%;
  height: 50px;
  width: 50px;
  object-fit: cover;
}
</style>
