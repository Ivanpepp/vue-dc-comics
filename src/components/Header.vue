<template>
  <div>
      <!-- nav section -->
        <nav class="my-view">
               
            <ul class="header-list">
                <li id="dc-logo">
                    <img  src="../assets/img/dc-logo.png" alt="Dc main logo">
                </li>
                <li  v-for='(element, index) in nav' :key="index" :class="{'active' : index == counter}"  @click='indexCounter(index)'>
                    <a href="#"> {{element}} </a>
                </li>
                <!-- <li><a href="#">comics</a></li>
                <li><a href="#">movies</a></li>
                <li><a href="#">tv</a></li>
                <li><a href="#">games</a></li>
                <li><a href="#">collectibles</a></li>
                <li><a href="#">videos</a></li>
                <li><a href="#">fans</a></li>
                <li><a href="#">news</a></li>
                <li><a href="#">shop</a></li> -->
            </ul>
        </nav>
        <!--/ nav section -->

        <!-- Bottom Header Section -->
        <div class="content">
            <div class="my-view">
                <h2>---[ Content goes here ]---</h2>
            </div>
        </div>
        <!--/ Bottom Header Section -->
  </div>
</template>

<script>
export default {
    name: 'Header',
    data: function(){
        return{
            nav: [
                'characters','comics','movies','tv','games','collectibles','videos','fans','news','shop'
            ],
            counter : 0,
        }
    },
    methods: {
        indexCounter : function(indexElement){
            this.counter = indexElement;
            
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';
    nav{
        display: flex;
        align-items: center;
        padding-top: 20px ;
        font-size: 1.3rem;
        
    }
    #dc-logo{
            &:hover{
                border-bottom: 6px solid transparent;
            }
            img{   
            vertical-align: middle;
            margin-right: 400px;
        }
    };
 
    .header-list{
        display: flex;
        list-style: none;
        transition: all .5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        line-height: 120px;
        li{
            border-bottom: 6px solid transparent;
            text-align: center;
            padding: 0 10px;
        }
        .active{
            border-bottom: 6px solid $primaryColor; 
            a{
                color: $primaryColor;
            }
        }
        li>a{
            
            text-transform: uppercase;
            text-decoration: none;
            color: $headerTextColor;
        
           
        }

        li:hover{
            border-bottom: 6px solid $primaryColor;
        }

       
    }
    .content{
        background-color: #1c1c1c;
        height: 140px;
        color: white;
        line-height: 140px;
    }
</style>