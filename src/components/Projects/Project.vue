<template>
  <a v-bind:href="link" target="blank" style="height: 100%;">
    <div class="project">
      <div class="project__image">
        <img v-bind:src="imgLink" />
      </div>
      <div class="project__content">
        <h4>{{ title }}</h4>
        <p>{{ description }}</p>
      </div>
    </div>
  </a>
</template>

<script>
export default {
  props: ["imgName", "title", "description", "link"],
  data: function () {
    const imgLink = require("@/assets/projects/" + this.imgName);
    return { imgLink };
  },
};
</script>

<style scoped>
.project {
  display: flex;
  flex-direction: column;
  border-radius: 10px;
  width: 350px;
  margin: 10px 0;
  transition: 0.5s all;
}
.project:hover {
  transform: scale(1.05);
}
.project__image img {
  width: 100%;
  border-radius: 10px 10px 0 0;
}
.project__content {
  border-radius: 0 0 10px 10px;
  background-color: #fff;
  padding: 20px 10px;
}
.project__content h4 {
  font-weight: 600;
}
.project__content p {
  font-size: 10pt;  
}
</style>
