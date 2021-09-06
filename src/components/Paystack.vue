<template>
    <paystack
    :amount="amount * 100"
    :email="email"
    :paystackkey="PUBLIC_KEY"
    :reference="reference"
    :callback="processPayment"
    :close="close"
  >
    Make Payment
 </paystack>
</template>



<script>
import paystack from "vue-paystack";
export default {
  name: "Paystack",
  components: {
    paystack
  },
  data: () => {
    return {
      amount: null,
      full_name: null,
      email:null
    };
  }
};
</script>