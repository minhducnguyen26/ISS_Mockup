<template>
    <div class="home_page_wrapper">
        <MyNavBar></MyNavBar>
        <MyBanner></MyBanner>
        <MyDescription></MyDescription>
        <MyEventsCalendar></MyEventsCalendar>
        <MyTestimonial></MyTestimonial>
        <MyShortcuts></MyShortcuts>
        
        <div class="office_hours_wrapper">
            <img src="../assets/office_hours.png" alt="Office Hours">
        </div>

        <div class="contact_us_wrapper">
            <img src="../assets/contact_us.png" alt="Contact Us">
        </div>
    </div>
</template>

<script>
import MyNavBar from "../components/MyNavBar.vue"
import MyBanner from "../components/MyBanner.vue"
import MyDescription from "../components/MyDescription.vue"
import MyEventsCalendar from "../components/MyEventsCalendar.vue"
import MyTestimonial from "../components/MyTestimonials.vue"
import MyShortcuts from "../components/MyShortcuts.vue"

export default {
    components: {
        MyNavBar,
        MyBanner,
        MyDescription,
        MyEventsCalendar,
        MyTestimonial,
        MyShortcuts
    }
}
</script>

<style scoped>
.home_page_wrapper {
    margin: 0 20% 60px;
    position: relative;
}

.contact_us_wrapper > img,
.office_hours_wrapper > img{
    width: 112%;
    margin: 0px -65px;
}

.office_hours_wrapper > img {
    margin-top: 30px;
}
</style>