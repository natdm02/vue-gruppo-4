<script>

import axios from 'axios';
  
export default {
  data() {
    return {
      apiUrl: 'http://127.0.0.1:8000/api/posts',  
      postslist: [],  
    };
  },
  created() {
    
    axios
      .get(this.apiUrl)
      .then((response) => {
       
        console.log(response);
        this.postslist = response.data.data;  
      })
      .catch((error) => {
       
        console.log(error);
      })
  },
};
</script>

<template>
  <div>
	  <h1>Post</h1>
	  <ul>
		<li v-for="post in posts" :key="post.id">{{ post.title }}</li>
	  </ul>
	</div>
</template>


<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400;1,500;1,700&display=swap');
	@import "styles/main";
	@import "./styles/main.scss";

    body {
		font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
	}

</style>




