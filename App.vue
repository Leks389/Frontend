<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="THANK YOU" />
      
    </div>
  </header>

  <main>
    <TheWelcome />
    <div class="button"><h1>Кнопка</h1></div>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}


@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
  .button{
width: 200px;
    padding: 5px 0;
    margin: 30px auto 0;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: bold;
    text-align: center;
    background: rgba(41, 41, 41, 0.88);
    color: #e6a833;
    -webkit-animation-name: 'play_down';
    -moz-animation-name: 'play_up';
    animation-duration: 1s;
    animation-iteration-count: infinite;
    box-shadow: 0 0 0 3px rgba(0, 0, 0,.5);
    cursor: pointer;
}

@keyframes  play_top {

	0% 
	{
		-webkit-box-shadow: 0 0 rgba(0,163,182,.6);
		-moz-box-shadow: 0 0 rgba(0,163,182,.6);
		box-shadow: 0 0 rgba(0,163,182,.6);
	}
	to 
	{
		-webkit-box-shadow: 0 0 0 20px rgba(0,163,182,0);
		-moz-box-shadow: 0 0 0 20px rgba(0,163,182,0);
		box-shadow: 0 0 0 20px rgba(0,163,182,0);
	}   

}

@keyframes  play_down {

	0% 
	{
		-webkit-box-shadow: 0 0 rgba(55,55,55,.6);
		-moz-box-shadow: 0 0 rgba(55,55,55,.6);
		box-shadow: 0 0 rgba(55,55,55,.6); 
	}
	to 
	{
		-webkit-box-shadow: 0 0 0 20px rgba(55,55,55,0);
		-moz-box-shadow: 0 0 0 20px rgba(55,55,55,0);
		box-shadow: 0 0 0 20px rgba(55,55,55,0);  
	}

}
  .logo {
    margin: 0 2rem 0 0;
  }


  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
