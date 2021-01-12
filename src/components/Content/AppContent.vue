<template>
  <div class="content">
    <AppContentAbout />
    <AppContentMulti />
    <AppContentProjects />
    <AppContentMobile />
    <AppContentMenu />
    <AppContentPost />
    <AppContentPartners />
  </div>
</template>

<script>
import AppContentAbout from "./About/AppContentAbout";
import AppContentMulti from "./Multi/AppContentMulti";
import AppContentProjects from "./Projects/AppContentProjects";
import AppContentMobile from "./Mobile/AppContentMobile";
import AppContentMenu from "./Menu/AppContentMenu";
import AppContentPost from "./Post/AppContentPost";
import AppContentPartners from "./Partners/AppContentPartners";

export default {
  name: "AppContent",
  components: {
    AppContentAbout,
    AppContentMulti,
    AppContentProjects,
    AppContentMobile,
    AppContentMenu,
    AppContentPost,
    AppContentPartners
  }
};
</script>

<style></style>
