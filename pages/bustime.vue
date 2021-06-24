<template>
    <div>
        <section class="hero is-small is-link">
      <div class="hero-body">
        <p class="title">
          <i class="fas fa-bus"></i> 현대인의 상쾌한 아침 
        </p>
        <p class="subtitle">
            늦지 않게 가자~ 버스 시간
        </p>
      </div>
    </section>
    <figure class="image is-middle">
        <img src="~assets/bus.PNG" alt="">
    </figure>
    <section class="hero is-success is-middle">
        &nbsp;&nbsp;&nbsp;&nbsp;목원대에서 출발하는 버스 시간표
    </section>
    <section class="columns">
            <div class="column">
                <table class="table is-striped is-hovable is-fullwidth">
                    <thead>
                        <th>회차</th>
                        <th>106번</th>
                        <th>706번</th>
                        <th>603번</th>
                        <th>312번</th>
                    </thead>
                    <tbody>
                        <template v-for = "pos in table106.length">
                            <tr :key = "pos">
                                <td>{{ pos }}</td>
                                <td>{{ table106[pos - 1]}}</td>
                                <td>{{ table706[pos - 1]}}</td>
                                <td>{{ table603[pos - 1]}}</td>
                                <td>{{ table312[pos - 1]}}</td>
                                
                            </tr> 
                        </template>
                    </tbody>
                </table>
            </div>
    </section>
    </div>

    
</template>

<script>
    import axios from 'axios';
    export default{
        async asyncData(){
            const bustime = await axios.get("https://raw.githubusercontent.com/wnshckdn/katerwnsgh_1/main/assets/bustime.json");
        
            return {
              table106: bustime.data.bus106,
              table706: bustime.data.bus706,
              table603: bustime.data.bus603,
              table312: bustime.data.bus312
            };
        }
    }
</script>

<style scoped>
    .image{
        width: 780px;
        height: auto;
        margin: auto;
        margin-top: 20px;
    }
</style>