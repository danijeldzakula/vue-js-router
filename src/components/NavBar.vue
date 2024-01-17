<template>
    <header class="header">
        <div class="container">
            <RouterLink to="/" class="logo-brand">House</RouterLink>
            
            <nav class="nav">
                <div class="navigation" :class=" [ toggle && isActive ]">
                    <ul class="menu" >
                        <li v-on:click="toggle = false">
                            <RouterLink class="link" to="/">Home</RouterLink>
                        </li>
                        <li v-on:click="toggle = false">
                            <RouterLink class="link" to="/about">About</RouterLink>
                        </li>  
                        <li v-on:click="toggle = false">
                            <RouterLink class="link" to="/contact">Contact</RouterLink>
                        </li>          
                    </ul>
                </div>

                <ul class="trigger">
                    <li>
                        <button v-on:click="toggle = !toggle" type="button" class="btn">Menu</button>
                    </li>                          
                </ul>
            </nav>
        </div>
    </header>
</template>



<script>
const focus = {
  mounted: (el) => {
    console.log(el)
  }
}

export default {
    name: 'NavBar',
    components: {
    },
    props: {
    },
    data() {
        return {
            toggle: false,
            isActive: 'isActive'
        }
    },    
    computed: {
        console: () => console,
        window: () => window,
    },

    directives: {
        focus
    },    

    methods: { 
        debug(el) {
            console.log(el)
        },
    }
}
</script>

<style lang="scss">
@use '@/assets/scss/abstracts/variables' as *;

.btn {
    margin: 0;
    padding: 10px 15px;
    color: $light;
    font-weight: #{$fontWeightBase * 5};
    border-radius: #{$radisBase * 2};
    border: 0;
    height: 38px;
    background-color: darken($officialColor, 8%);
}
</style>