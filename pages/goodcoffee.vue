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
                        <th>번호</th>
                        <th>이름</th>
                        <th>원산지</th>
                        <th>맛</th>
                    </thead>
                    <tbody>
                        <template v-for = "pos in morningCoffee.length">
                            <tr :key = "pos">
                                <td>{{ pos }}</td>
                                <td>{{ tableMorningCoffee[pos - 1].Name}}</td>
                                <td>{{ tableMorningCoffee[pos - 1].from}}</td>
                                <td>{{ tableMorningCoffee[pos - 1].Taste}}</td>
                                
                            </tr> 
                        </template>
                    </tbody>
                </table>
            </div>
            <div class="column">
                <table class="table">
                    <thead>
                        <th>사이트</th>
                        <th>이름</th>
                    </thead>
                    <tbody>
                        <tr>
                            <td>커피창고</td>
                            <td><a href="https://smartstore.naver.com/coffeecg/products/2140616478?NaPm=ct%3Dkpow3vgo%7Cci%3D06603c1d6b17895eaa99c2974d11f962b7d5aa4e%7Ctr%3Dsls%7Csn%3D408933%7Chk%3D3b2564f95458006c781440943bd7c44b47d587bb">페이지 이동</a></td>
                        </tr>
                        <tr>
                            <td>원두창고</td>
                            <td><a href="https://smartstore.naver.com/mart3132/products/4977227027?NaPm=ct%3Dkpow4aw8%7Cci%3D6a46d9e71afb4b9eb37208d178db497793a465f4%7Ctr%3Dsls%7Csn%3D1354157%7Chk%3D2007972d86f0e45601251ec69e19801196812dec">페이지 이동</a></td>
                        </tr>
                        <tr>
                            <td>로스팅몰</td>
                            <td><a href="https://smartstore.naver.com/romill/products/345591507?NaPm=ct%3Dkpow4ytc%7Cci%3D6fe8796ff07a1fbe2094975e4ba207d8faac9299%7Ctr%3Dsls%7Csn%3D299606%7Chk%3D623c2e93bf239d9bfbc3045dec9b1fdb08ae2374">페이지 이동</a></td>
                        </tr>
                        
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
            const morningCoffee = await axios.get("https://github.com/wnshckdn/katerwnsgh_1/blob/main/assets/coffee.json");
            console.log(Object.keys(morningCoffee))
            console.log(morningCoffee.data.data.morningCoffee)
        
            return {
                tableMorningCoffee : morningCoffee.data.data.morningCoffee
            };
        }
    }
</script>