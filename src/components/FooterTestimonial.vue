<template>

    <section class="footer-testimonial">
        <div class="container">
            <h2>PostPilot is 🔥 for <span>DTC</span></h2>

            <div ref="users" class="users">

                <div class="user" v-for="(user, index) in n" :key="index">

                    <div class="user-info">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTtOmFEdYBQJuCTnbe7DzQjspZ_-mGfN3NxNw&s"
                            alt="profile" />
                        <div class="user-name">
                            <h5>{{ user.name }}</h5>
                            <p>{{ user.username }}</p>
                        </div>
                        <i class="ri-twitter-fill twitter-icon"></i>
                    </div>
                    <p class="content">
                        Using <strong>PostPilot</strong> for years. Good for re-engagement.
                        And you can get creative with messaging.
                    </p>


                </div>
            </div>
            <!-- Button -->
            <div class="cta-btn">
                <button>TRY IT RISK-FREE</button>
            </div>


        </div>
    </section>
</template>
<script>
export default {
    name: "UserCarousel",

    data() {
        return {
            n: [{ "name": "Sehzad", "username": "@sehzad" },
            { "name": "Vraj", "username": "@vraj" },
            { "name": "Chintan", "username": "@chintan" },
            { "name": "Ruhaan", "username": "@ruhaan" },
            { "name": "Arsalan", "username": "@arsalan" },

            ]
        }
    },


    mounted() {
        const slider = this.$refs.users;
        let isDown = false;
        let startX;
        let scrollLeft;

        slider.addEventListener("mousedown", (e) => {
            isDown = true;
            slider.classList.add("active");
            startX = e.pageX - slider.offsetLeft;
            scrollLeft = slider.scrollLeft;
        });

        slider.addEventListener("mouseleave", () => {
            isDown = false;
            slider.classList.remove("active");
        });

        slider.addEventListener("mouseup", () => {
            isDown = false;
            slider.classList.remove("active");
        });

        slider.addEventListener("mousemove", (e) => {
            if (!isDown) return;
            e.preventDefault();
            const x = e.pageX - slider.offsetLeft;
            const walk = (x - startX) * 2; // scroll speed multiplier
            slider.scrollLeft = scrollLeft - walk;
        });
    },
};
</script>
<style lang="">

</style>