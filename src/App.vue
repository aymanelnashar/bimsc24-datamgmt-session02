the script is where the js code goes
<script setup>
import { Text, ref } from "vue" // you need this to use ref()

    const inputtext = ref("");
    const displayText = ref("");
    const colour = ref("");

    const addText = () => {
        displayText.value += inputtext.value;
    };

    let updatecolour = ref('white');
    let newcolour = ref('');
    
    function changecolour () {
        colour.value = newcolour.value;
    }
        
</script>



<!-- the template is where the html code goes -->
<template>

    <body>
    
    <div id="navbar" class="container">  
        <div id="title">Ayman website</div>
        
        <div id="logo">
            <img src="./ELEVER 004.jpg" alt="Ayman Chair">

        </div>
        

    </div>

        <div id="flex">

            <div id="sidebar" class="container"> Sidebar

            <input v-model="inputtext" placeholder="Add Text" />
                    <button @click="addText()">Add Text</button>  

            <input v-model="colour" type="text" placeholder="Add Color">
            <button @click="updatecolour" class="container" >Apply Color</button>    

        </div>
            <div id="main" class="container"> <p>{{ displayText }}</p> </div>     
        
    </div>


    </body>
    

</template>



<!-- style is where the css code goes -->
<style scoped>

    html{
        
        background-color: rgb(59, 59, 59); 
        color: white;
    }

    body{

        margin:0;
    }

    div{

        /* put the borders in the inside of container */
        box-sizing: border-box;
    }

    img{

        height: 100%;
        width: auto;

    }

    #navbar{

        height: 100px;
        font-size: 30px;
        border-color: red;


    }

    #flex{
        
        display: flex;
        height: calc(100vh - 50px);
    }

    #sidebar{
        
        width:30%;
        border-color: blue;
        border-width: 3px;
        background-color: rgb(77, 3, 3);
        font-size: 30px;

    }

    #main{
        width:70%;
        border-color: rgb(2, 49, 2);
        border-width: 3px;
        background-color: rgb(155, 155, 155);
        font-size: larger;
        color: rgb(0, 0, 0);

    }

    #title{
        width: 70%;
        float:left;
    }

    #logo{
        width: 30%;
        height: 100%;
        float:right;
        text-align: right;

    }

    .container{

        border-style: dotted;
        border-width: 3px;
        background-color: rgb(0, 0, 0);
        font-style: normal;
        color: white;

    }

</style>

