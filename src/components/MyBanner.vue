<template>
    <div class="my_banner_wrapper">
        <div class="background_image">
            <div class="background_overlay"></div>

            <div class="banner_titles">
                <div class="school_name">Dixie State University</div>
                <div class="office_name">International Office</div>
            </div>

            <div class="nav_button_list">
                <div class="single_nav_button" v-for="button in nav_button_list" :key="button.context">
                    <MyButton :context="button.context" 
                        type="nav_button" 
                        :dropdown_context="button.dropdown_context"></MyButton>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import MyButton from "../components/MyButton.vue"

export default {
    components: {
        MyButton
    },
    data() {
        return {
            nav_button_list: [
                {
                    context: "Perspective Student",
                    dropdown_context: [
                        "Cost of Attendance",
                        "Scholarships",
                        "Academic Programs",
                        "Apply Now"
                    ]
                },
                {
                    context: "New Student",
                    dropdown_context: [
                        "Visit Campus",
                        "On-Campus Resources",
                        "Health Insurance"
                    ]
                },
                {
                    context: "Current Student",
                    dropdown_context: [
                        "Employment & Taxes",
                        "Additional Scholarships"
                    ]
                },
                {
                    context: "Partnerships",
                    dropdown_context: [
                        "International Friend",
                        "Community Connection Family"
                    ]
                }
            ]
        }
    }
}
</script>

<style scoped>
.my_banner_wrapper {
    position: relative;
    margin: 0 -35% 50%;
}

.background_image {
    background-image: url(../assets/banner_background.jpeg);
    background-size: cover;
    background-position: center;
    position: absolute;
    height: 480px;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 0;
}

.background_image > img {
    height: 100%;
    max-width: 100%;
}

.background_overlay {
    background-color: rgba(0,0,0,.5);
    width: 100%;
    height: 100%;
}

.nav_button_list {
    display: flex;
    justify-content: end;
    margin-top: -35px;
}

.single_nav_button {
    margin-left: 40px;
}

.banner_titles {
    position: absolute;
    top: 15%;
    left: 20%;
    color: white;
}

.school_name {
    font-size: 25px;
}

.office_name {
    font-size: 80px;
    text-transform: uppercase;
    font-weight: bold;
}
</style>