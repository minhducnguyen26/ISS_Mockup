<template>
    <router-view/>
</template>

<style>
/* Reset CSS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Source Sans Pro', sans-serif;
}
/* Color Palette */
:root {
    --main-red: #ba1c21;
    --main-grey: #c7c5c5;
}

@media only screen and (max-width: 1280px) {
    .home_page_wrapper {
        margin: 0 5% 60px !important;
    }
    .normal_button_style {
        font-size: 17px !important;
    }
    .nav_button_style {
        padding: 0px 25px !important;
    }
    .search_button {
        padding: 8.5px !important;
    }
    .search_button > span {
        font-size: 25px !important;
    }
    .my_banner_wrapper {
        margin: 0px -6% 50% !important;
    }
    .office_name {
        font-size: 70px !important;
    }
    .dropdown_context_list {
        top: 48px !important;
    }
    .single_context > p {
        font-size: 18px !important;
        padding: 0 20px !important;
    }
    .first_line, .second_line{
        font-size: 18px !important;
        line-height: 32px !important;
    }
}
</style>