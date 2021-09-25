<template>
    <div class="home_page_wrapper">
        <MyNavBar></MyNavBar>
        <MyBanner></MyBanner>
        <MyDescription></MyDescription>
        <MyEventsCalendar></MyEventsCalendar>
        <MyTestimonial></MyTestimonial>
        <MySocialContact></MySocialContact>
        <MyContactUs></MyContactUs>
    </div>
</template>

<script>
import MyNavBar from "../components/MyNavBar.vue"
import MyBanner from "../components/MyBanner.vue"
import MyDescription from "../components/MyDescription.vue"
import MyEventsCalendar from "../components/MyEventsCalendar.vue"
import MyTestimonial from "../components/MyTestimonials.vue"
import MySocialContact from "../components/MySocialContact.vue"
import MyContactUs from "../components/MyContactUs.vue"

export default {
    components: {
        MyNavBar,
        MyBanner,
        MyDescription,
        MyEventsCalendar,
        MyTestimonial,
        MySocialContact,
        MyContactUs
    }
}
</script>

<style scoped>
.home_page_wrapper {
    margin: 0 20%;
}
</style>