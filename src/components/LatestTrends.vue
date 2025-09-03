<template>
    <section class="trends-section">
        <h2 class="section-title">
            Latest trends <span class="highlight">& insights</span>
        </h2>

        <div class="card-grid">
            <div class="card" v-for="(item, index) in articles" :key="index">
                <img :src="item.image" :alt="item.title" class="card-image" />
                <h3 class="card-title">{{ item.title }}</h3>
            </div>
        </div>

    </section>
</template>
<script>
export default {

    data() {
        return {
            articles: [
                {
                    title: '3 Low-Cost Campaigns You Must Run to Win BFCM',
                    image: new URL('@/assets/lowcost.png', import.meta.url).href
                },
                {
                    title: 'Postcard Marketing: The Definitive Guide to High ROI [2022]',
                    image: new URL('@/assets/postcard.png', import.meta.url).href
                },
                {
                    title: 'The Ultimate Guide to Thank You Notes for Ecommerce',
                    image: new URL('@/assets/the_ultimat.png', import.meta.url).href
                }
            ]
        }
    },

}
</script>
<style lang="">

</style>