<template>
  <section class="tm-section" id="cartList">
    <div class="row">
      <div class="col-lg-12 tm-section-header-container">
        <h2 class="tm-section-header gold-text tm-handwriting-font">
          <img src="img/logo.png" alt="Logo" class="tm-site-logo" /> 購買商品
        </h2>
        <div class="tm-hr-container">
          <hr class="tm-hr" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="tm-daily-menu-container margin-top-60">
        <div class="col-lg-4 col-md-4">
          <img src="img/menu-board.png" alt="Menu board" class="tm-daily-menu-img" />
        </div>
        <div class="col-lg-8 col-md-8">
          <table class="table table-bordered cart-table">
            <thead>
              <tr>
                <th scope="col">#</th>
                <th scope="col">品項</th>
                <th scope="col">單價</th>
                <th scope="col">數量</th>
                <th scope="col">小計</th>
                <th scope="col"></th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th scope="row">1</th>
                <td>拿鐵</td>
                <td>$45</td>
                <td>
                  <input type="number" value="2" min="1" />
                </td>
                <td>$90</td>
                <td>
                  <a href>
                    <i class="fa fa-trash-o" aria-hidden="true"></i>
                  </a>
                </td>
              </tr>
              <tr>
                <th scope="row">2</th>
                <td>拿鐵</td>
                <td>$45</td>
                <td>
                  <input type="number" value="2" min="1" />
                </td>
                <td>$90</td>
                <td>
                  <a href>
                    <i class="fa fa-trash-o" aria-hidden="true"></i>
                  </a>
                </td>
              </tr>
              <tr>
                <th scope="row"></th>
                <td colspan="3"></td>
                <td class="redText">$180</td>
              </tr>
            </tbody>
          </table>

          <a href="#" class="tm-more-button margin-top-30 btn-center">確認結帳</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CartList"
};
</script>