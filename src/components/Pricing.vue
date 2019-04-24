<template>
  <div class="pricing flex-center">
    <div class="main container">
      <h1 class="title">Choose Your Plan</h1>
      <p
        class="description"
      >When someone does something that they know that they shouldn’t do, did they.</p>
      <div class="plans flex-row-around">
        <div
          class="plan flex-center"
          v-for="{id, title, description, features, price} in plans"
          :key="id"
        >
          <div class="image-section flex-center">
            <img class="image" src="../images/image.svg" alt="image">
          </div>
          <h3>{{title}}</h3>
          <p>{{description}}</p>
          <ul class="features-list">
            <li class="feature" v-for="feature in features" :key="feature.index">{{feature}}</li>
          </ul>
          <h1>{{price}}</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Pricing",
  data: () => ({
    plans: [
      {
        id: 0,
        title: "Starter",
        description: "For the Beginner",
        features: [
          "Secure Online Transfer",
          "Unlimited Styles for Interface",
          "Reliable Customer Service"
        ],
        price: "$99.00"
      },
      {
        id: 1,
        title: "Developer",
        description: "For the Tinkerer",
        features: [
          "Secure Online Transfer",
          "Unlimited Styles for Interface",
          "Reliable Customer Service"
        ],
        price: "$195.00"
      },
      {
        id: 2,
        title: "Startup",
        description: "For the Entrepreneur",
        features: [
          "Secure Online Transfer",
          "Unlimited Styles for Interface",
          "Reliable Customer Service"
        ],
        price: "$295.00"
      },
      {
        id: 3,
        title: "Enterprise",
        description: "For the Industrialist",
        features: [
          "Secure Online Transfer",
          "Unlimited Styles for Interface",
          "Reliable Customer Service"
        ],
        price: "$399.00"
      }
    ]
  })
};
</script>

<style scoped>
.main {
  text-align: center;
}
.plans {
  flex-wrap: wrap;
}

.plan {
  flex-direction: column;
  background-color: #f0f0f0;
  width: 250px;
  margin: 15px;
  padding: 10px 0;
}

.features-list {
  padding: 0 20px;
}

.features-list li {
  list-style: none;
}

.image {
  margin-top: 20px;
  width: 140px;
  height: 140px;
  border-radius: 50%;
  object-fit: cover;
}
</style>
