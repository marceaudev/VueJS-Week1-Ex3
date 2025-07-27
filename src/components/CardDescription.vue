<script setup>
import FirstParagraph from './FirstParagraph.vue'
import SecondParagraph from './SecondParagraph.vue'
import ThirdParagraph from './ThirdParagraph.vue'
import Title from './Title.vue'

const props = defineProps({
  personInfos: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <section>
    <img
      src="https://res.cloudinary.com/lereacteur-apollo/image/upload/v1704967000/RNCP31114/cours-vue/exo-sem-1/mystery-person_bueack.jpg"
      alt="Photo de base"
    />
    <div>
      <Title
        :firstname="personInfos.firstname"
        :lastname="personInfos.lastname"
        :gender="personInfos.gender"
      />
      <FirstParagraph :gender="personInfos.gender" :age="personInfos.age" :job="personInfos.job" />
      <SecondParagraph :firstname="personInfos.firstname" :hobbies="personInfos.hobbies" />
      <ThirdParagraph :gender="personInfos.gender" :pet="personInfos.pet" />
    </div>
    <font-awesome-icon :icon="['fas', 'heart']" />
  </section>
</template>

<style scoped>
section {
  width: calc((100% - 40px) / 4);
  background-color: #efeeee;
  padding: 10px;
  display: flex;
  flex-direction: column;
  border-radius: 10px;
  box-shadow: 0 0 7px v-bind('personInfos.favoriteColor');
}

section > div {
  flex: 1;
}

img {
  width: 100%;
  aspect-ratio: 16/10;
  object-fit: cover;
  object-position: top;
  border-radius: 5px;
}

svg {
  align-self: flex-end;
  font-size: 26px;
  color: grey;
  cursor: pointer;
}

@media (max-width: 1250px) {
  section {
    flex: none;
    width: 300px;
  }
}
</style>
