<template>
    <div class="my_testimonials_wrapper">
        <div class="header">
            <div class="section_title">Testimonial</div>
            <div class="header_text">What Our Students Say</div>
            <div class="underline"></div>
        </div>

        <div class="body_wrapper">
            <div class="arrow_left">
                <span class="material-icons">arrow_back_ios</span>
            </div>

            <div class="main_content_wrapper">
                <div class="testimonial_wrapper">
                    <div class="single_testimonial">
                        <div class="testimonial_content">
                            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
                        </div>

                        <div class="student_infos">
                            <div class="student_image">
                                <img src="../assets/student1.jpeg" alt="Student Image">
                            </div>

                            <div class="student_name">LangHui He</div>

                            <div class="student_major">Computer Science</div>
                        </div>
                    </div>

                    <div class="single_testimonial">
                        <div class="testimonial_content">
                            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
                        </div>

                        <div class="student_infos">
                            <div class="student_image">
                                <img src="../assets/student2.jpeg" alt="Student Image">
                            </div>

                            <div class="student_name">Duy Huynh</div>

                            <div class="student_major">Computer Science</div>
                        </div>
                    </div>
                </div>

                <div class="tracking_dots">
                    <div class="dot_wrapper dot_wrapper_active">
                        <div class="dot_center dot_1"></div>
                    </div>
                    
                    <div class="dot_wrapper">
                        <div class="dot_center dot_2"></div>
                    </div>

                    <div class="dot_wrapper">
                        <div class="dot_center dot_3"></div>
                    </div>

                    <div class="dot_wrapper">
                        <div class="dot_center dot_4"></div>
                    </div>
                </div>
            </div>

            <div class="arrow_right">
                <span class="material-icons">arrow_forward_ios</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin: 60px 0;
}

.section_title {
    font-size: 45px;
    font-weight: 700;
}

.header_text {
    margin: 20px 0;
    font-size: 30px;
    color: var(--main-red);
}

.underline {
    width: 40px;
    height: 3px;
    background-color: var(--main-grey);
}

.body_wrapper {
    display: grid;
    grid-template-columns: 10% 80% 10%;
}

.arrow_left {
    display: flex;
    align-items: center;
    cursor: pointer;
}

.arrow_right {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    cursor: pointer;
}

.tracking_dots {
    display: flex;
    justify-content: center;
    margin: 60px 0 30px;
    cursor: pointer;
}

.dot_wrapper {
    height: 23px;
    width: 23px;
    border-radius: 50%;
    margin: 0 5px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.dot_wrapper_active {
    border: 1px solid var(--main-grey);
}

.dot_center {
    height: 15px;
    width: 15px;
    border-radius: 50%;
    background-color: var(--main-grey);
}

.testimonial_wrapper {
    display: flex;
}

.single_testimonial {
    margin: 0 10px 0 20px;
    box-shadow: 0px 8px 16px 0px rgb(0 0 0 / 20%);
}

.testimonial_content {
    margin: 30px;
}

.student_infos {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.student_image > img {
    width: 100px;
}

.student_name {
    margin: 5px 0;
}

.student_major {
    margin-bottom: 20px;
}
</style>