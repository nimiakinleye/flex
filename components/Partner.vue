<template>
  <div>
    <div class="container">
      <div class="page-header">
        Become A <span class="text-orange-500">Partner</span>
      </div>
      <div class="py-12 px-6 sm:px-0 my-bg flex flex-col text-center rounded-lg">
        <div class="mb-5 md:px-48 text-gray-900 text-lg font-semibold">
          We are looking to work with facilitators of fun, enjoyment and
          relaxation. Specificaly, business owners in the hospitality, tourism,
          travel, and other similar industry. <br> Please get in touch. Let’s create
          magic together.
        </div>
        <div
          class="mx-auto w-full sm:w-3/5 lg:w-2/5 bg-white shadow-lg px-6 py-12 rounded-lg ring ring-orange-500"
        >
          <div class="">
            <div class="text-red-500">{{ message }}</div>
            <form action="">
              <div class="my-8">
                <input v-model="newPartner.businessName" placeholder="Enter Business name" type="text" />
              </div>
              <div class="my-8">
                <input v-model="newPartner.email" placeholder="Enter your email address" type="text" />
              </div>
              <div class="my-8">
                <input v-model="newPartner.tel" placeholder="Enter your phone number" type="text" />
              </div>
              <div class="my-8">
                <input v-model="newPartner.referral" placeholder="Enter name of contact person" type="text" />
              </div>
              <div class="my-8">
                <select v-model="newPartner.industryCategory" name="" id="">
                  <option value="Industry">Industry</option>
                  <option value="E-commerce">E-commerce</option>
                </select>
              </div>
              <button
                @click.prevent="submit"
                class="w-full bg-orange-500 hover:bg-orange-600 text-white font-semibold p-2 rounded-md"
              >
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
      newPartner: {
        businessName: '',
        email: '',
        tel: '',
        referral: '',
        industryCategory: ''
      },
      message: ''
    }    
  },
  methods: {
    async addPartner(){
      await this.$axios.$post('https://flex-e3041-default-rtdb.firebaseio.com/partners', 
      {
          partner: this.newPartner
      },
      {
        
      })
    },
    submit () {
      if (this.newPartner.businessName === '') {
        this.message = 'Please enter your business name'
      } else if (this.newPartner.email === '') {
        this.message = 'Please enter your email'
      } else if (this.newPartner.tel === '') {
        this.message = 'Please input your phone number'
      } else if (this.newPartner.referral === '') {
        this.message = 'Please tell us how you got to know about us'
      } else if (this.newPartner.industryCategory === '') {
        this.message = 'Please tell us your area of expertise'
      } else{
        // this.message = 'Application Sent!';
        this.addPartner();
      }
    }
  }
}
</script>

<style>
</style>