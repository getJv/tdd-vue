<template>
  <div>
    <v-user-search-form @submitted="searchUser"></v-user-search-form>
    <v-user-profile :user="user"></v-user-profile>
  </div>
</template>
<script>
import { mapState } from "vuex";
import VUserSearchForm from "@/components/VUserSearchForm";
import VUserProfile from "@/components/VUserProfile";
export default {
  components: { VUserSearchForm, VUserProfile },
  methods: {
    searchUser(username) {
      this.$store.dispatch("SEARCH_USER", { username });
    }
  },
  computed: {
    ...mapState({
      user: "user"
    })
  }
};
</script>

