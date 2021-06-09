<template>
    <div>
        <section class="hero is-success">
      <div class="hero-body">
        <p class="title">
          현대인의 상쾌한 아침 <i class="far fa-bell"></i>
        </p>
        <p class="subtitle">
            활기를 불어넣어줄 다양한 커피
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
                        <template v-for = "pos in morningCoffee.length">
                            <tr :key = "pos">
                                <td>{{ pos }}</td>
                                <td>{{ tableMorningCoffee[pos - 1].Name}}</td>
                                <td>{{ tableMorningCoffee[pos - 1].from}}</td>
                                <td>{{ tableMorningCoffee[pos - 1].Taste}}</td>
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
            const morningCoffee = await axios.get('https://api.edamam.com/api/food-database/v2/parser');
            return {
              tableMorningCoffee: morningCoffee.data.message,
              tableMornigKeys: Object.keys(morningCoffee.data.message),
            };
        },
    };
</script>
