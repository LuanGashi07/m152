<template>
    <div class="main">
    <h1>Noten</h1>

    <ul class="todos">
        <li v-for="item in grades">{{ item.name }}</li>
        <br>
        <li v-for="item in grades">{{ item.grades }}</li>
    </ul>

    <input type="text" placeholder="Fach eingeben" v-model="newItem" />
    <input type="text" placeholder="Note" v-model="newItem" />
    <input type="submit" value="Hinzufügen" v-on:click="addItem(newItem)" />
</div>
</template>
<script>
export default {
    data: function() {
        return {
            grades: [
{
        name: "Mathematik",
        grades: [5,4.7,3.5,4.1] 
    },
    {
        name: "Geschichte",
        grades: [5.5,4.9,5.75] 
    },
    {
        name: "Physik",
        grades: [2,2.7,4.3] 
    },
    {
        name: "Deutsch",
        grades: [4.25,4.1,3.5] 
    }
            ]
        }
    },
        methods: {
        addItem: function(item) {
            this.tasks.push(item);
        }
    }, 
    grades: [
    {
        name: "Mathematik",
        grades: [5,4.7,3.5,4.1] 
    },
    {
        name: "Geschichte",
        grades: [5.5,4.9,5.75] 
    },
    {
        name: "Physik",
        grades: [2,2.7,4.3] 
    },
    {
        name: "Deutsch",
        grades: [4.25,4.1,3.5] 
    }
    ]
}
</script>

<style lang="scss">
    .main {
        max-width: 500px;
        margin: 0 auto;
        background-color: #eee;
        padding: 20px;

        h1 {
            text-align: center;
        }
    }
</style>