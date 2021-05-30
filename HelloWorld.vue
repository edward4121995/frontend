<template>
  <h1>Todo List</h1>
  <div>
  <input v-model="myText">
  <button @click="tambah">Add</button>
  <ul>
    <li v-for='item in todos'>{{ item.desc }}</li>
  </ul>
  </div>
</template>

<script >

export default{
  data: function(){
    return {
      todos: [
        {desc: 'Bangun Tidur'},
        {desc: 'Mandi'},
        {desc: 'Makan'}
      ],
      myText : ''
    }
  },
  methods: {
    tambah: function(){
      this.todos.push({ desc: this.myText})
    }
  }
}

</script>


