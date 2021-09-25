<template>  
    <div class="my_nav_bar_wrapper">
        <div class="dsu_logo">
            <img src="../assets/dsu_logo.png" alt="DSU Logo">
        </div>

        <div class="main_nav_bar">
            <div class="single_link" v-for="link in nav_link_list" v-bind:key="link">
                <MyButton :context=link type="normal"></MyButton>
            </div>
        </div>

        <div class="my_dixie_and_search_actions">
            <div class="my_dixie_button">
                <MyButton context="My Dixie" type="nav_button"></MyButton>
            </div>

            <div class="search_button">
                <span class="material-icons">search</span>
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
            nav_link_list: ["Academics", "Admissions", "Campus Life", "Alumni", "Giving", "Athletics"]
        }        
    }
}
</script>

<style scoped>
.my_nav_bar_wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 40px 0;
}

.dsu_logo > img{
    width: 145px;
}

.main_nav_bar {
    display: flex;
}

.single_link {
    margin: 0 5px;
    text-transform: uppercase;
}

.my_dixie_and_search_actions {
    display: flex;
    align-items: center;
}

.my_dixie_button {
    margin-right: 7px;
}

.search_button {
    background-color: var(--main-grey);
    padding: 11.5px;
    transform: skew(-25deg);
    cursor: pointer;
    margin-left: -12px;
}

.search_button > span {
    transform: skew(25deg);
    font-size: 30px;
}
</style>