<script setup>

defineProps({
  firstName: {
    type: String,
    required: true,
  },
  scientific_name: {
    type: String,
    required: false,
  },
  environment: {
    type: String,
    required: true,
  }
})
</script>

<template>
  Alien Species: {{ firstName }}
    <section class="card">
      <aside class="left-side">
        <div class="headshot"/>
        <span class="environment">{{ environment }}</span>
      </aside>
      <aside class="right-side">
        <div class="name">{{ scientific_name }}, {{ firstName }}</div>
      </aside>
    </section>
</template>

<style scoped>
section.card {
  display: flex;
  border: 1px solid lightgray;
  border-radius: 10px;
  gap: 1rem;
  padding: 0.5rem;

  &:hover {
    border-color: black;
    cursor: pointer;
  }

  .left-side, .right-side {
    display: flex;
    flex-direction: column;
  }

  .left-side {
    flex-basis: 40%;
    display: flex;
    gap: 0.5rem;

    .headshot {
      height: 120px;
      width: 90px;
      background-color: lightgray;
    }

    .dob {
      font-size: 0.8rem;
      font-style: italic;
    }
  }

  .right-side {
    .name {
      font-size: 1.2rem;
      font-weight: bold;
    }
  }
}
</style>