<template>
  <div>
    <div class="container">
      <div class="page-header">
        Join <span class="text-orange-500">Us</span>
      </div>
      <div class="py-12 my-bg flex text-center rounded-lg">
        <div class="mx-auto bg-white shadow-lg px-6 py-12 rounded-lg ring ring-orange-500">
          <div class="font-semibold">Join Our Waiting List</div>
          <div>Enjoy the benefits of having fun while you work</div>
          <div class="">
            <div class="text-red-500">{{ message }}</div>
            <form action="">
              <div class="my-4">
                <input v-model="newUser.name" placeholder="Enter your full name" type="text">
              </div>
              <div class="my-8">
                <input v-model="newUser.email" placeholder="Enter your email address" type="email">
              </div>
              <div class="my-8">
                <input v-model="newUser.tel" placeholder="Enter your phone number" type="text">
              </div>
              <div class="my-8">
                <select v-model="newUser.source" name="" id="">
                  <option value="Instagram">Instagram</option>
                  <option value="Facebook">Facebook</option>
                </select>
              </div>
              <button @click.prevent="submit" class="w-full bg-orange-500 hover:bg-orange-600 text-white font-semibold p-2 rounded-md">
                Join
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      newUser: {
        name: '',
        email: '',
        tel: '',
        source: ''
      },
      message: ''
    }
  },
  methods: {
    submit () {
      if (this.newUser.name === '') {
        this.message = 'Please enter a name'
      } else if (this.newUser.email === '') {
        this.message = 'Please enter your email'
      } else if (this.newUser.tel === '') {
        this.message = 'Please input your phone number'
      } else if (this.newUser.source === '') {
        this.message = 'Please tell us how you got to know about us'
      } else{
        this.message = 'Application Sent!';
        console.log(this.newUser)
      }
    }
  }
}
</script>

<style>

</style>