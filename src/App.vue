<template>
  
  <div id="app" class="main">

      <div class="main-content" v-if="!$route.meta.isLogin">
        <NavbarSec/>
      </div>

      <main :class="{'overview-blk':$route.name === 'Overview'}">

        <router-view/>

      </main>

    </div>


</template>


<script>
import NavbarSec from './components/Navbar/NavbarSec.vue'
import('@/css/Style.css')


export default {
  name: 'App',
  components:{
    NavbarSec

  },
  mounted() {
    console.log(this.$route.meta)
  }
}
</script>


<style >



#app{
 /* background-color: #ebe6e6; */
  background-color: #fff;
}


.main-content{
  margin-left: 280px;
  margin-top: 70px;

}

body{
  overflow: hidden;
}

main{
  /* background: #dddddd; */

  /* background: #ffffff; */
  min-height: calc(100vh - 50px);
  overflow: hidden;
  /* height: 90vh; */
}

.overview-blk {
  background: #fff;
}
a:hover{
  list-style-type: none;
  text-decoration: none;
}

.news{
  display: flex;
}

/* .announcement{
  margin: 18px 9px 0px 0px;
  padding: 18px 20px 24px 23px;
  width: -webkit-fill-available;
  background: #fff;
} */

/* .flashNews{
  margin: 18px 0px 0px 9px;
  padding: 18px 20px 24px 23px;
  width: -webkit-fill-available;
  background: #fff;
} */

/* .msg{
  margin-top: 18px;
  padding: 18px 20px 24px 23px;
  background: #fff;
} */






</style>