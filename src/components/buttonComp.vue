<template>
  <div id="butt" class="button">
    <h1>{{ msg }}</h1>
    Click on the Button for initiating context menu
    <br>
    <button class="btn btn-primary" @contextmenu.prevent="openMenu($event)">
      {{username}}! right click me!
    </button>
  </div>
</template>

<script>
  export default {
    name: 'buttonComp',
    props: {
      msg: String,          // Title
      username: String,
    },
    methods: {
      openMenu(e) {
        ```
        OpenMenu() changes 'click' to true and then initiates setMenu() and sets the focus on the <ul>
        ```
        console.log("OpenMenu Initiated");
        this.click = true;
        this.$nextTick( () => {
            this.$$.mymenu.focus();
            this.setMenu(e.y, e.x);
          }
        )
      },
      setMenu(top, left) {
        ```
        setMenu() changes the offset of the <ul> to be at the mouses' coordinates
        ```
        console.log('SetMenu initiated!');
        this.top = `${top}px`;
        this.left = `${left}px`;
      },
      closeMenu(){
        ```
        Initiates when @blur occures.
        ```
        this.click = false;
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>