<template>
  <div>
    <div class="container">
      <div class="page-header">Frequently Asked <span class="text-orange-500">Questions</span></div>
      <div class="mt-20">
        <div class="md:max-w-4xl mx-auto px-3" v-for="(faq, i) in faqs" :key="i">
          <div class="my-6 cursor-pointer" @click="toggleShow(faq)">
            <div class="flex items-center justify-between px-12 py-3 rounded-t-lg text-white shadow-lg font-semibold text-lg my-bg">
              <div>{{ faq.question }}</div>
              <div @click="toggleShow(faq)" class="cursor-pointer p-1">{{ faq.view }}</div>
            </div>
            <div class="">
              <div class="slide-down w-full px-12 py-5 bg-white shadow-lg rounded-b-lg" v-show="faq.show" v-html="faq.answer"></div>
            </div>
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
      faqs: [
        { question: 'What is flex?', show: false, view: '+', answer: `Flex is an easy-to-use mobile app that helps you save specifically for fun and enjoyment.
        <br />
        <br />
        We believe that every hardworking person should enjoy their wealth as much as they save for other life goals.
        <br />
        <br />
        We combine discipline and fun together by making it super easy for people to plan towards having fun and enjoyment.
        <br />
        <br />
        You can choose to save daily, weekly or monthly for your personalized enjoyment.` 
        },
        { question: 'How Can I Contact Flex?', show: false, view: '+', answer: `We are always at your service. Call 09051470106 or email us at contact@myflex.fun.` 
        },
        { question: 'Is Flex In Charge Of My Money?', show: false, view: '+', answer: `While your account and money is 100% safe with us, we also use a third party payment processor, Flutterwave to make sure your transactions are secured and super easy!` 
        },
        { question: 'How Does Flex Notify Me?', show: false, view: '+', answer: `Flex sends personalized and general emails to all our users. We also use push notifications to make sure you don’t miss any important update and information.` 
        },
        { question: 'How Can I Contact Flex?', show: false, view: '+', answer: `We are always at your service. Call 09051470106 or email us at contact@myflex.fun.` 
        },
        { question: 'How Safe Is Flex?', show: false, view: '+', answer: `All financial information is encrypted and stored to PCIDSS Level 1 compliant standards. PCIDSS Level 1 compliance is a set of rules stated by credit card companies and audited by an independent third party.
        <br/>
        <br />
        It is the highest possible rating one can get in the electronic payment processing industry. Additionally, all transmission to our banking partner and on our site is via an encrypted 256-bit HTTPS SSL connection.` 
        },
        { question: 'What Is OTP?', show: false, view: '+', answer: `OTP means One-Time Password that is initiated for transfers and withdrawals on your flex account.` 
        },
        { question: 'Are My Card Details Secure?', show: false, view: '+', answer: `Yes. We work with a PCIDSS-compliant payment processor, Flutterwave to handle your card details. 
        Your card details are extremely safe and are stored in a way that they can never be compromised
        ` 
        },
        { question: 'How can I secure my account?', show: false, view: '+', answer: `Use a unique password that is known to only you. Activate the 2FA on your account or use the fingerprint login option.` 
        },
        { question: 'Do I have To Be On The App To Save For My Flex?', show: false, view: '+', answer: `No, you don’t have to. Once you have set up your flex plan, and set the amount, it will deduct automatically from your bank account on the set date. However, if you want to use the Quick Top-Up option, you’d have to log in to do that.` 
        },
        { question: 'How Do I Create A Flex Plan?', show: false, view: '+', answer: `Log into the app and select create flex plan. Follow the prompt and click “Create My Flex”. You will be able to see your flex plan in your dashboard.` 
        },
        { question: 'Can I Withdraw My Flex Target Savings?', show: false, view: '+', answer: `Although, we strongly advise that you wait till maturity date but In a case you wish to break the target, kindly note that you will be charged extra 1% of the processing fee. However, if you wait till maturity date, you will only be charged 1% processing fee.` 
        },
        { question: 'Can I Edit My Savings Anytime?', show: false, view: '+', answer: `Yes, you can. Click on your flex plan and click the “edit option” . You can either decrease or increase the amount. Set the new amount you want to save and the frequency. Click Submit.` 
        },
        { question: 'What If I Don’t Have Money In My Account On The Set Day?', show: false, view: '+', answer: `<div>We will not be able to debit you for that day, week or month. We will only be able to save for you when you have funds in your debit card. However, you have the option to use the <span class="font-bold">"Quick Top-Up"</span> option once you have funded your account.</div>` 
        },
        { question: 'How Does Stash Works?', show: false, view: '+', answer: `Stash is a manual savings option different from the automatic flex target savings. It allows you to withdraw anytime unlike your flex plan that is set to maturity date. With stash you can quickly pay for flex events or trips. You can add funds to your stash using the Quick Top-Up Option.` 
        },
        { question: 'How Does Quick Top-Up Works?', show: false, view: '+', answer: `Quick Top-Up is very handy especially on days when you missed the automatic savings or days when you want to save some lucky funds from your account.You can either top up your stash or your flex plan. It won’t affect your automatic savings at all.` 
        },
        { question: 'How do I pay for flex trips?', show: false, view: '+', answer: `To join any flex trip, log into your app and select “Join Flex Trips”. Pick from the varieties of trips available and click the “Join Flex” button.` 
        },
        { question: 'How do I pay for flex events?', show: false, view: '+', answer: `Log into the app, select “find fun events”. Pick from the varieties of events and click “Join Flex”.` 
        },
        { question: 'Is Flex In Charge Of All The Trips & Events?', show: false, view: '+', answer: `Flex is the primary stakeholder of all trips and events. However, we partner with other trusted stakeholders in the hospitality industry to ensure that our flexers are well taken care of on trips and events.` 
        },
        { question: 'What If I Could No Longer Go On A Trip Or Attend An Event?', show: false, view: '+', answer: `If you didn’t make a trip or event, please contact us by sending an email to contact@myflex.fun and inform us, within 48 hours, the funds for the trip or event will be returned to your stash wallet.` 
        },
        { question: 'How Will I Get Details Of Events & Trips?', show: false, view: '+', answer: `We advise that you read about any interested event or trips in your dashboard using the “Learn More” button. However, you will also receive emails about  any event or trip you joined. Details such as meetup point, items you need to bring along or specifics etc. will be explained via emails.` 
        },
      ]
    }
  },
  methods: {
    toggleShow (faq) {
      if (faq.view === '+') {
        this.faqs.forEach(faq => {
          faq.show = false;
          faq.view = '+'
        })
        faq.show = true;
        faq.view = '-';
      } else {
        faq.show = false;
        faq.view = '+'
      }
      
    }
  }
}
</script>

<style>
.slide-down{
  animation-name: slide-down;
  animation-duration: 1000ms;
}

@keyframes slide-down {
  0% { transform: translateY(-50px); opacity: 0; }
}
</style>