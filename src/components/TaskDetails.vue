<template>
  <!-- <div class="task">
    <h3>{{ task.title }}</h3>
   
  </div> -->

  <div class="container">
    <div class="card my-5">
      <div class="card-content">
        <div class="content is-flex is-justify-content-space-between">
          <p class="title is-4">{{ task.title }}</p>
          <div class="icons">
            <i class="material-icons"> delete </i>
            <i class="material-icons" :class="{ active: task.isFav }">
              favorite
            </i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["task"],
};
</script>

<style>
</style>