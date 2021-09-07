<template>
  <div class="home">
	  <div class="aaa" @click="$router.push({path:'/About'})"> 这是vr项目</div>
    <div id="viewer"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import {Viewer} from 'photo-sphere-viewer'
    import 'photo-sphere-viewer/dist/photo-sphere-viewer.css'
    export default {
        data(){
            return{
                viewer:'',
                imgurl1:require('../assets/a.png'),
            }
        },
        mounted(){
            this.viewer = new Viewer({
                container:document.querySelector('#viewer'),
                panorama:this.imgurl1,
                size:{
                    width: '100vw',
                    height: '100vh',
                },
            });
        }
    }
</script>

<style type="text/less">
	.home{
		position: relative;
	}
	
	
	.aaa{
		position: absolute;
		left: 0;
		top: 0;
		z-index: 99;
	}
	
</style>