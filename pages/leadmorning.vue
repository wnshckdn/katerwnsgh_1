<template>
    <div>
        <section class="hero is-success">
      <div class="hero-body">
        <p class="title">
          직장인의 알람기능 <i class="far fa-bell"></i>
        </p>
        <p class="subtitle">
          늦지않게 일하러가자
        </p>
      </div>
    </section>
    <section id>
        <div column="col1"></div>
        <div column="col2"></div>
    </section>
    </div>
</template>
<script>
import  leadmorning  from "@/assets/bicycle.json";

export default {
    data() {
        return {
            tableBicycle: worldBicycle.names,
            tableBicycleFrom: worldBicycle.from,
            tableBicycleProduct: worldBicycle.Product
        }
    }
}
</script>
