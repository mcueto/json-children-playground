<template>
  <div class="hello">
    <div class="smartphone">
      <div class="content text-center p-4">
        <h1>
          {{ json.title }}
        </h1>
        <p>
          {{ json.description }}
        </p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'MobilePhone',
  props: {
    json: Object
  },
  data: function () {
    return {
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* The device with borders */
.smartphone {
  position: relative;
  /* width: 360px;
  height: 640px; */
  margin: auto;
  border: 16px black solid;
  border-top-width: 60px;
  border-bottom-width: 60px;
  border-radius: 36px;
  background: red;
}

/* The horizontal line on the top of the device */
.smartphone:before {
  content: '';
  display: block;
  width: 60px;
  height: 5px;
  position: absolute;
  top: -30px;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #333;
  border-radius: 10px;
}

/* The circle on the bottom of the device */
.smartphone:after {
  content: '';
  display: block;
  width: 35px;
  height: 35px;
  position: absolute;
  left: 50%;
  bottom: -65px;
  transform: translate(-50%, -50%);
  background: #333;
  border-radius: 50%;
}

/* The screen (or content) of the device */
.smartphone .content {
  /* width: 360px; */
  min-height: 600px;
  background: white;
  font-family: 'Fredoka One', cursive;
  background-color: #c2b1ad;
  background-image: url("https://www.transparenttextures.com/patterns/gray-floral.png");
}
</style>
