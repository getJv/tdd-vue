<template>
  <div class="user-profile">
    <img class="user-profile__avatar" :src="user.avatar_url" />
    <div class="user-profile__name">{{ user.name }}</div>
    <div class="user-profile__bio">{{ user.bio }}</div>
  </div>
</template>
<script>
export default {
  props: {
    user: Object,
    required: true,
    default: () => ({})
  }
};
</script>

