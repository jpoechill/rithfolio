<template>
  <div>

    <div class="container pt-2">
      <div class="row pt-4 pb-1">
        <div class="offset-md-2 col-md-8">
          <p>
            Yumm, algorithms..?!
          </p>
          Name <br>
          <input type="text" class="w-100 mb-2"><br>
          Message <br>
          <textarea class="w-100 mb-2" rows="5"></textarea>
          <button class="w-100 p-2">Send Message</button>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  transition: 'fade'
}
</script>

<style scoped>
input[type=text], textarea {
  border-radius: 20px;
  border: 2px solid #f2f2f2;
  padding: .5rem 1rem;
  margin: .4rem 0;
}

button {
  border-radius: 20px;
  border: 0;
  background-color: #f7f7f7;
  color: #4A90E2;
  font-size: 20px;
  font-weight: 700;
}
</style>
