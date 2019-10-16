<template>
  <!-- show block start -->
  <div class="detail-area">
    <div class="row">
      <div class="full-stretch">
        <div class="col-lg-6 col-md-12 col-sm-12 flex-center">
          <img src="img/popular-1.jpg" alt="Popular" class="tm-popular-item-img" />
        </div>
        <div class="col-lg-6 col-md-12 col-sm-12 flex-center">
          <div class="select-wrap">
            <div>
              <h3>{{pid}}</h3>
            </div>

            <div>
              <select name="size">
                <option value="big">大杯$60</option>
                <option value="mid">中杯$55</option>
                <option value="small">小杯$45</option>
              </select>
            </div>

            <div>
              <input type="number" min="1" value="1" class="cup" />
              <span>杯</span>
            </div>

            <div>
              <select name="templ">
                <option value="cold">冷</option>
                <option value="hot">熱</option>
              </select>
            </div>

            <div>
              <select name="sugar">
                <option value="fulls">全糖</option>
                <option value="halfs">半糖</option>
                <option value="nones">無糖</option>
              </select>
            </div>

            <button>加入購物車</button>
          </div>
        </div>
      </div>
      <i class="fa fa-times" aria-hidden="true" @click="closeDesc"></i>
    </div>
  </div>
  <!-- show block end -->
</template>
    
<script>
export default {
  name: "DescLayer",
  props: {
    pid: {
      type: Number,
      required: true
    }
  },
  methods: {
    closeDesc() {
      const moreContent = document.querySelector(".tm-popular-items-container");
      const closebtn = document.querySelector(".detail-area .fa-times");
      moreContent.classList.add("of");
      setTimeout(() => {
        moreContent.classList.remove("active-show", "active", "of");
      }, 600);
    }
  }
};
</script>