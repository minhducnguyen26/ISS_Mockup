<template>
    <div class="my_shortcuts_wrapper" v-if="page_on_scroll">
        <div class="button_wrapper apply_now_button">
            <img src="../assets/application.png" alt="Application">
        </div>

        <div class="button_wrapper calendar_button">
            <img src="../assets/calendar.png" alt="Calendar">
        </div>

        <div class="button_wrapper social_media_button" @click="open_social_media_list">
            <img src="../assets/link.png" alt="Social Media Links">
        </div>

        <div class="button_wrapper chat_now_button">
            <img src="../assets/chat_bubbles.png" alt="Chat Bubbles">
        </div>

        <div class="social_media_list_wrapper" v-if="show_social_media_list">
            <i class="lab la-instagram"></i>
            <i class="lab la-facebook-f"></i>
            <i class="lab la-whatsapp"></i>
            <i class="lab la-youtube"></i>
        </div>
    </div>
</template>

<script>
export default {
    mounted() {
        window.addEventListener('scroll', this.handle_page_on_scroll);
    },
    data() {
        return {
            page_on_scroll: false,
            show_social_media_list: false
        }
    },
    methods: {
        handle_page_on_scroll() {
            let last_scroll = 0;
            let current_scroll = document.documentElement.scrollTop || document.body.scrollTop;

            //! Scroll Down
            if ( current_scroll > 0 && last_scroll <= current_scroll ) {
                last_scroll = current_scroll;
                this.page_on_scroll = true;
            }
            //! Scroll Up
            else {
                last_scroll = current_scroll;
                this.page_on_scroll = false;
            }

            this.show_social_media_list = false;
        },
        open_social_media_list() {
            this.show_social_media_list = !this.show_social_media_list;
        }
    }
}
</script>

<style scoped>
.button_wrapper {
    position: fixed;
    bottom: 5%;
    background-color: var(--main-red);
    border-radius: 50%;
    padding: 10px 13px;
    cursor: pointer;
    box-shadow: 0px 8px 16px 0px rgb(0 0 0 / 20%);
}

.button_wrapper > img {
    width: 30px;
}

.apply_now_button {
    left: 36%;
}

.calendar_button {
    left: 44%;
}

.social_media_button {
    left: 51.5%;
}

.chat_now_button {
    left: 59%;
}

.social_media_list_wrapper {
    position: fixed;
    top: 320px;
    left: 50.8%;
    display: flex;
    flex-direction: column;
    border: 1px solid var(--main-grey);
    background-color: white;
    border-radius: 25px;
}

.social_media_list_wrapper > i {
    font-size: 50px;
    margin: 10px;
    color: var(--main-red);
    cursor: pointer;
}
</style>