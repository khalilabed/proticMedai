<template>
  <footer class="footer-section">
    <div class="overlay"></div>
    <div class="footer-content">
      <h3 class="majallab36 pt-5">لا تتردد في التواصل معنا</h3>
      <p class="py-2 majalla28">شاركنا اللحظات الجميلة وكون جزء من عيلتنا</p>
      <div class="box-input-resop">
        <input
          type="text"
          class="form-control w-size majalla20"
          id="exampleInputName"
          aria-describedby="emailHelp"
          placeholder="سجل بإيميلك وكون على اطلاع بكل جديد"
        />
        <button type="button" class="btn btn-light majalla18 me-2">إشترك الآن</button>
      </div>
      <div class="box-bottom">
        <p class="majalla20">
          للراغبين في إضافة فعالياتهم إلى المنصة الرجاء التواصل عن طريق البريد
          الإلكتروني
        </p>
        <p class="majalla18">Techshef@gmail.com</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterSection",
};
</script>

<style scoped>
.footer-section {
  position: relative;
  background-image: url("../assets/bg-footer2.png");
  background-size: cover;
  background-position: center;
  text-align: center;
  padding: 20px 0;
  height: 450px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.box-bottom {
  padding-top: 60px;
}
</style>