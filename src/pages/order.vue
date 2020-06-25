<template>
    <div> 
        home
        <order-header>1</order-header>
        <router-view>2</router-view>
        <order-footer>3</order-footer>     
    </div>
</template>
<script>
import OrderHeader from './../components/OrderHeader'
import OrderFooter from './../components/OrderFooter'
export default {
    
    name:'nav-home',
    components:{
        OrderHeader,
        OrderFooter
    }
}
</script>