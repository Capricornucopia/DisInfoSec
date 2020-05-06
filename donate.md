![DisInfoSec](DisInfoSec_Logo.png)

## Donate to DisInfoSec!

DisInfoSec is raising funds for organizations that are **run by disabled people** for **disabled people.** 

<!-- Load Stripe.js on your website. -->
<script src="https://js.stripe.com/v3"></script>

<!-- Create a button that your customers click to complete their purchase. Customize the styling to suit your branding. -->
<button
  style="background-color:#6772E5;color:#FFF;padding:8px 12px;border:0;border-radius:4px;font-size:1em"
  id="checkout-button-sku_HEHmYVIpnFx6a7"
  role="link"
>
  Checkout
</button>

<div id="error-message"></div>

<script>
(function() {
  var stripe = Stripe('pk_live_5VhQ17oda6ZrCR9aS4targh8');

  var checkoutButton = document.getElementById('checkout-button-sku_HEHmYVIpnFx6a7');
  checkoutButton.addEventListener('click', function () {
    // When the customer clicks on the button, redirect
    // them to Checkout.
    stripe.redirectToCheckout({
      items: [{sku: 'sku_HEHmYVIpnFx6a7', quantity: 1}],

      // Do not rely on the redirect to the successUrl for fulfilling
      // purchases, customers may not always reach the success_url after
      // a successful payment.
      // Instead use one of the strategies described in
      // https://stripe.com/docs/payments/checkout/fulfillment
      successUrl: 'https://disinfosec.tech/thanks.md',
      cancelUrl: 'https://disinfosec.tech/donate.md',
    })
    .then(function (result) {
      if (result.error) {
        // If `redirectToCheckout` fails due to a browser or network
        // error, display the localized error message to your customer.
        var displayError = document.getElementById('error-message');
        displayError.textContent = result.error.message;
      }
    });
  });
})();
</script>


![Autistic Self Advocacy Network logo](unnamed.gif)

The Autistic Self Advocacy Network was founded by autistic people to advocate for the rights of autistic people. [Their mission statement from their website is](https://autisticadvocacy.org/about-asan/):

"The Autistic Self Advocacy Network seeks to advance the principles of the disability rights movement with regard to autism. ASAN believes that the goal of autism advocacy should be a world in which autistic people enjoy equal access, rights, and opportunities. We work to empower autistic people across the world to take control of our own lives and the future of our common community, and seek to organize the autistic community to ensure our voices are heard in the national conversation about us. Nothing About Us, Without Us!"

![Autistic Women & Nonbinary Network logo](20200426_145136.jpg)

The Autistic Women & Nonbinary Network was founded by autistic people to advocate for the rights of autistic people who are female or nonbinary. [Their mission statement from their website is](https://awnnetwork.org/about/):

"The mission of Autistic Women & Nonbinary Network (AWN) is to provide community, support, and resources for Autistic women, girls, nonbinary people, and all others of marginalized genders.

AWN Network  is dedicated to building a supportive community where we can share our experiences in an understanding, diverse and inclusive environment. AWN is committed to recognizing and celebrating diversity and the many intersectional experiences in our community.

We welcome all women, transgender and cisgender, non-binary and genderqueer people, Two-Spirit people, people who have at anytime identified as women or girls, and all other people of marginalized genders or of no gender. AWN recognizes and affirms all people’s gender identities and expressions, as well as choices about disclosure, transition, and going stealth.

Our goal is to dispel stereotypes and misinformation which perpetuate unnecessary fears surrounding an autism diagnosis. We seek to share information which works to build acceptance and understanding of disability. Welcome to AWN Network!"

**More disabled-run charities will be added here.**

Some funds will go toward paying disabled event workers and making the event accessible to the Deaf and hard of hearing.
