<template>
  <div class="tab-container">
            <!-- Boîte des onglets -->
            <div class="tabs">
                <div data-open="view1" class="tab active" @click="isActive=!isActive">
                    <p>Onglet 1</p>
                </div>
                <div data-open="view2" class="tab" @click="active">
                    <p>Onglet 2</p>
                </div>
                <div data-open="view3" class="tab">
                    <p>Onglet 3</p>
                </div>
                <div data-open="view4" class="tab">
                    <p>Onglet 4</p>
                </div>
            </div>

            <!-- Boîte des vues -->
            <div class="views">

                <div class="view active" data-id="view1">
                    <h2>Premier onglet</h2>
                    <p>Lorem ipsum dolor sit amet consectetur.</p>
                </div>

                <div class="view" data-id="view2">
                    <h2>Deuxième onglet</h2>
                    <p>Lorem, ipsum dolor.</p>
                </div>

                <div class="view" data-id="view3">
                    <h2>Troisième onglet</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta aliquid, cum suscipit non labore alias cumque perspiciatis corporis quasi nobis quis earum nam, laudantium ut amet! Quas fugiat accusantium at pariatur excepturi nihil quisquam repellendus tempore sunt id labore dolorum iste earum eligendi aliquam debitis, voluptates quidem maxime. Optio, illum.</p>
                </div>

                <div class="view" data-id="view4">
                    <h2>Quatrième onglet</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda, libero alias. Mollitia aliquid quidem harum maxime deleniti voluptatibus vel adipisci.</p>
                </div>
            </div>
        </div>

</template>

<script>
  export default {
    name: 'TabsCompo',
    data() {
      return {
        isActive:true,
        view1: true,
        view2: false,
        view3: false,
        view4: false
      }
    }
  }

</script>

<style>
  body{
    background-color: #cecece;
    color: #464646;
    margin: 0;
}

h1{
    text-align: center;
}

.tab-container{
    width: 75%;
    margin: auto;
    padding: 10px;
}

.tab-container .tabs{
    display: flex;
    flex-direction: row;
}

.tab-container .tabs .tab{
    background-color: #B7B7B7;
    padding: 5px 20px;
    cursor: pointer;
    margin-right: 3px;
    transition: all .2s ease;
    -webkit-transition: all .2s ease;
    -moz-transition: all .2s ease;
    -ms-transition: all .2s ease;
    -o-transition: all .2s ease;
}

.tab-container .tabs .tab.active{
    background-color: #FF3333;
    color: #FFFFFF;
    cursor: auto;
}

.tab-container .views .view{
    background-color: #FF3333;
    color: #FFFFFF;
    padding: 5px 20px;
    transition: all .2s ease;
    -webkit-transition: all .2s ease;
    -moz-transition: all .2s ease;
    -ms-transition: all .2s ease;
    -o-transition: all .2s ease;
    display: none;
}

.tab-container .views .view.active{
    display: block;
}

</style>
