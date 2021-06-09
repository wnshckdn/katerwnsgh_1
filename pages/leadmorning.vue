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
    <section class="columns">
            <div class="column">
                <table class="table">
                    <thead>
                        <th></th>
                        <th></th>
                    </thead>
                    <tbody>
                        <template v-for = "pos in morningfood.length">
                            <tr :key = "pos">
                                <td>{{ pos }}</td>
                                <td>{{ tableDogKeys [pos - 1]}}</td>
                                <td>
                                    <span></span>
                                    </td>    
                            </tr> 
                        </template>
                    </tbody>
                </table>
            </div>
            <div class="column">
            </div>
    </section>
    </div>

    
</template>


<script>
    import axios from 'axios';
    export default {
        async asyncData(){
            const morningfood = await axios.get('https://api.edamam.com/api/food-database/v2/parser');
            return {
              tableMorningBreeds: morningfood.data.message,
              tableMornigKeys: Object.keys(morningfood.data.message),
            };
        },
    };
</script>
