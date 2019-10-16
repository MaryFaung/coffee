<template>
  <section class="tm-section tm-section-margin-bottom-0 row">
    <div class="col-lg-12 tm-section-header-container">
      <h2 class="tm-section-header gold-text tm-handwriting-font">
        <img src="img/logo.png" alt="Logo" class="tm-site-logo" />
        蛋糕加購專區
      </h2>
      <div class="tm-hr-container-short">
        <hr class="tm-hr" />
      </div>
    </div>
    <div class="col-lg-12 tm-popular-items-container">
      <!-- show block start -->
      <div class="detail-area">
        <div class="row">
          <div class="full-stretch">
            <div class="col-lg-6 col-md-12 col-sm-12 flex-center">
              <img src="img/popular-1.jpg" alt="Popular" class="tm-popular-item-img" />
            </div>
            <div class="col-lg-6 col-md-12 col-sm-12 flex-center">wwww</div>
          </div>
          <i class="fa fa-times" aria-hidden="true"></i>
        </div>
      </div>
      <!-- show block end -->

      <div class="tm-popular-item">
        <img src="img/popular-1.jpg" alt="Popular" class="tm-popular-item-img" />
        <div class="tm-popular-item-description">
          <h3 class="tm-handwriting-font tm-popular-item-title">
            <span class="tm-handwriting-font bigger-first-letter">a</span>mericano
          </h3>
          <hr class="tm-popular-item-hr" />
          <p>
            Maecenas tempus, tellus eget condimentum rhoncus, sem quam semper
            libero, sit amet adipiscing sem neque. sed ipsum.
          </p>
          <div class="order-now-container">
            <a
              href="javascript:void(0);"
              class="order-now-link tm-handwriting-font"
              data-id="1"
              @click="showDesc"
            >Order Now</a>
          </div>
        </div>
      </div>
      <div class="tm-popular-item">
        <img src="img/popular-2.jpg" alt="Popular" class="tm-popular-item-img" />
        <div class="tm-popular-item-description">
          <h3 class="tm-handwriting-font tm-popular-item-title">
            <span class="tm-handwriting-font bigger-first-letter">c</span>appuccino
          </h3>
          <hr class="tm-popular-item-hr" />
          <p>
            Maecenas tempus, tellus eget condimentum rhoncus, sem quam semper
            libero, sit amet adipiscing sem neque. sed ipsum.
          </p>
          <div class="order-now-container">
            <a href="javascript:void(0);" class="order-now-link tm-handwriting-font">Order Now</a>
          </div>
        </div>
      </div>
      <div class="tm-popular-item">
        <img src="img/popular-3.jpg" alt="Popular" class="tm-popular-item-img" />
        <div class="tm-popular-item-description">
          <h3 class="tm-handwriting-font tm-popular-item-title">
            <span class="tm-handwriting-font bigger-first-letter">m</span>ocha
          </h3>
          <hr class="tm-popular-item-hr" />
          <p>
            Maecenas tempus, tellus eget condimentum rhoncus, sem quam semper
            libero, sit amet adipiscing sem neque. sed ipsum.
          </p>
          <div class="order-now-container">
            <a href="javascript:void(0);" class="order-now-link tm-handwriting-font">Order Now</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import DescLayer from "@/components/content/DescLayer.vue";
export default {
  name: "CakeList",
  components: { DescLayer },
  data: function() {
    return {
      index: 0,
      title: "12aa",
      items: [{ name: "A" }, { name: "B" }]
    };
  },
  methods: {
    showDesc(event) {
      //console.log(event.target.dataset.id);
      console.log(this.items[event.target.dataset.id - 1].name);
      const moreContent = document.querySelector(".tm-popular-items-container");

      moreContent.classList.add("active");
      setTimeout(() => {
        if (moreContent.classList.contains("active")) {
          moreContent.classList.add("active-show");
        }
      }, 150);
    }
  }
};
</script>