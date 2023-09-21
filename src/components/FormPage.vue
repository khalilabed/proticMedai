<template>
  <section class="box-form py-3">
    <div class="container py-5">
      <div class="text-center">
        
      </div>
      <div class="row d-flex align-items-center justify-content-center">
        <div class="col-lg-6 col-md-12 text-white">
          <h3 class="text-blank majallab36 ">أطلب الكتيب بدون تردد</h3>
          <div class="d-flex py-3">
            <h2 class="majallab40 size">
              زد مبيعات متجرك %500 <br />بهذه الاستراتيجيات
              <img src="../assets/icon-hero.png" alt="" width="50px" />
            </h2>
          </div>
          <p class="majalla28">
            أسرار لا تخبرك بها شركات التسويق سوف تجدها في كتيبنا، <br />
            كن أول من يحصل عليه وستجني ثماره بإذن الله
          </p>
          <button type="submit" @click="scrollToTop" class="btn btn-primary px-5 mt-4 majalla20 blod-none">
            اطلب نسختك الان
          </button>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="bg-for">
            <img src="../assets/bg-form.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth"
      });
    }
  }
}
</script>