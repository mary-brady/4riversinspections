<template>
  <div class="container-fluid">
    <div class="row justify-content-center">
      <div class="hero-image col-12">
        <img src="../assets/Home1.jpeg" alt="home" />
      </div>
    </div>
    <div class="row justify-content-center">
      <div class="col-lg-12">
        <p>Dedicated to serving Idaho home buyers and real estate agents. Our goal is to make the process of home inspection as convenient, thorough, and affordable as possible</p>
      </div>
    </div>
    <div class="row justify-content-center">
      <div class="col-lg-4">
        <div class="card" style="width: 30rem;">
          <div class="card-body">
            <h5 class="card-title">WHY CHOOSE US?</h5>
            <h6 class="card-subtitle mb-2 text-muted">You're family!</h6>
            <p
              class="card-text"
            >When you choose us for your home inspections, you are family. As family, we keep the best interest of your investment at the forefront throughout our entire process.</p>
            <p
              class="card-text"
            >We love what we do and truly care about our customers. The impact of a home purchase is huge and we strive to NEVER treat you like another number on the books.</p>
            <p
              class="card-text"
            >4 Rivers inspectors love when home buyers join us on inspections, and in most cases, prefer it! As a home buyer, we understand you will have questions, and find the best way to answer is in-person as they arise.</p>
            <router-link to="/Contact">Contact Us</router-link>
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <div class="card" style="width: 30rem;">
          <div class="card-body">
            <h5 class="card-title">WHAT WE OFFER:</h5>
            <h6 class="card-subtitle mb-2 text-muted">something something</h6>
            <ul>
              <li>
                <p class="card-text">Same-day report delivery!</p>
              </li>
              <li>
                <p class="card-text">FREE Lifetime Subscription to Home Binder ($120 value!)</p>
              </li>
              <li>
                <p class="card-text">Listing Inspection</p>
              </li>
              <li>
                <a href="#" class="card-link">Residential Home Inspections</a>
              </li>
              <li>
                <a href="#" class="card-link">Healthy Home Check-Ups</a>
              </li>
              <li>
                <a href="#" class="card-link">Healthy Home Check-Ups</a>
              </li>
              <li>
                <a href="#" class="card-link">1-Year Builder's Warranty Inspections</a>
              </li>
              <li>
                <a href="#" class="card-link">Radon Gs Testing</a>
              </li>
              <li>
                <a href="#" class="card-link">Mold Testing</a>
              </li>
              <li>
                <a href="#" class="card-link">Well Productivity &amp; Water Quality Testing</a>
              </li>
              <li>
                <a href="#" class="card-link">Lead &amp; Asbestos Testing</a>
              </li>
              <li>
                <a href="#" class="card-link">Methamphetamine Testing</a>
              </li>
              <li>
                <a href="#" class="card-link">FREE Re-Inspection Post-Repairs</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <div class="card" style="width: 30rem;">
          <div class="card-body">
            <h5 class="card-title">HOME INSPECTIONS</h5>
            <h6 class="card-subtitle mb-2 text-muted">GUARANTEED</h6>
            <p
              class="card-text"
            >All of our home inspections are guaranteed. If you are not 100% satisfied with your inspection, we will give you your money back.</p>
            <p>Our home inspection team has an extensive background in the building industry. Paired with over 2,000 inspections in Oregon &amp; Idaho, that gives us an edge most home inspection companies don’t have.</p>
            <p>
              All of our home inspections
              <strong>are guaranteed</strong>. If you are not 100% satisfied with your inspection, we will give you your money back.
            </p>
            <a href="#" class="card-link">Card link</a>
            <a href="#" class="card-link">Another link</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>
<style scoped>
a {
  color: black;
}
</style>
