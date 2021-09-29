<template>
    <div class="my_button_wrapper">
        <!-- Normal Style Button -->
        <div class="button_type_wrapper" v-if="type ==='normal' && !dropdown_context">
            <div class="normal_button_style">
                {{ context }}
            </div>
        </div>

        <!-- Nav Button Style -->
        <div class="button_type_wrapper tilted_style" v-if="type === 'nav_button' && !dropdown_context">
            <div class="nav_button_style">
                <p class="nav_button_context">{{ context }}</p>
            </div>
        </div>

        <!-- Nav Button with Dropdown Context -->
        <div class="button_type_wrapper tilted_style" v-if="type === 'nav_button' && dropdown_context">
            <div class="nav_button_style">
                <p class="nav_button_context">{{ context }}</p>
                <span class="material-icons">expand_more</span>
                <div class="dropdown_context_list">
                    <div class="single_context" v-for="context in dropdown_context" :key="context">
                        <p>{{ context }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        context: String,
        type: String,
        dropdown_context: Array
    }
}
</script>

<style scoped>
.my_button_wrapper {
    font-size: 15px;
    cursor: pointer;
}

.normal_button_style {
    padding: 15px;
    font-size: 18px;
}

.normal_button_style:hover {
    background-color: var(--main-red);
    color: white;
}

.nav_button_style {
    background-color: var(--main-red);
    color: white;
    font-weight: 700;
    text-transform: uppercase;
    padding: 5px 35px;
    font-size: 20px;
    display: flex;
    align-items: center;
}

.nav_button_context, .nav_button_style > span{
    transform: skew(25deg);
}

.nav_button_style > span {
    margin-left: 10px;
}

.tilted_style {
    transform: skew(-25deg);
}

.nav_button_style {
    float: left;
    overflow: hidden;
}

.nav_button_style .nav_button_context {
    font-size: 16px;  
    border: none;
    outline: none;
    color: white;
    padding: 14px 16px;
    background-color: inherit;
    font-family: inherit;
    margin: 0;
}

.dropdown_context_list {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    width: 100%;
    top: 58px;
    left: 0;
    box-shadow: 0px 8px 16px 0px rgb(0 0 0 / 20%);
    z-index: 1;
}

.single_context {
    float: none;
    color: black;
    padding: 15px;
    text-align: center;
    display: block;
}

.single_context > p {
    transform: skew(25deg);
}

.single_context:hover {
    background-color: var(--main-grey);
}

.nav_button_style:hover .dropdown_context_list {
    display: block;
}
</style>