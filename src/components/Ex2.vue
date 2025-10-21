<script>

    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                addItem:""
            }
        },
            methods:{
                deleteItem(index){
                    this.items.splice(index,1);

                },
                addToList(){
                    if (this.addItem.trim()!=""){
                        this.items.push(this.addItem.trim())
                    }
                    this.addItem="";

                }
            }
    }

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for="(item,i) in items">
            {{ item }}
             <button @click="deleteItem(i)">Delete</button>
        </li>
     </ul>
     <input type="text" v-model="addItem"></input>
     <button @click="addToList">add!</button>
   
</template>
