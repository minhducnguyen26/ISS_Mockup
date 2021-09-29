<template>
    <div class="my_chart_and_stats_wrapper">
        <img class="pie_chart" src="../assets/pie_chart.png" alt="Pie Chart">
        <img class="block_graph" src="../assets/block_graph.png" alt="Block Graph">
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.my_chart_and_stats_wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 60px 0 90px;
}

.my_chart_and_stats_wrapper > img {
    width: 45%;
}

.pie_chart {
    margin-right: 20px;
}

.block_graph {
    margin-left: 40px;
    margin-right: 50px;
}
</style>