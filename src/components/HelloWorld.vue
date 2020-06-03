<template>
  <div class="hello">
    <li v-for="(item,index) in list">
       {{item.name}}
      <button @click="add(index)">learn</button>
    </li>
    <div class="result">
      <th>name</th>
      <th>number</th>
      <th>price</th>
      <tr v-for="(item,index) in result">
        <td>{{item.name}}</td>
        <td>{{item.number}}</td>
        <td>{{item.price}}</td>
      </tr>
    </div>
  </div>




</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      show: true,
      list:[
        {
          name:'vue',
          price:20,
        },
        {
          name:'react',
          price:30
        },
        {
          name:'flutter',
          price:50
        }


      ],
      result:[]
    }
  },
  methods: {
    add (index) {
      if()
      result.push(list[index])
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  /* display: inline-block; */
  margin: 0 10px;
}
th{
  padding:20px;
}
a {
  color: #42b983;
}
.transition-box {
  margin-bottom: 10px;
  width: 200px;
  height: 100px;
  border-radius: 4px;
  background-color: #409EFF;
  text-align: center;
  color: #fff;
  padding: 40px 20px;
  box-sizing: border-box;
  margin-right: 20px;
}
.container {
  display:grid;
  /* grid-template-columns:2fr 3fr minmax(100px, 1fr) ; */
  height:400px;
  width: 100%;
  gap: 10px 20px;
  grid-template-areas: 'a b c'
                       'd e f'
                       'g h j';
  place-content: space-around space-evenly

}
.box {
  margin:10px;
  width:22%;
  height:100px;
  background: #42b983;



}
</style>
