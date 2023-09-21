<template>
  <div class="bg-body">
    <div class="container pt-5">
      <div class="text-center pt-5">
        <h3 class="majallab36">مميزات لن تجدها في مكان آخر</h3>
      </div>
      <div class="py-5">
        <div>
          <div class="row">
            <div class="col-6 text-center">
              <div class="wraper">
                <ul class="btn-wraper">
                  <li
                    v-for="item in section1.slice(0, 2)"
                    :key="item.id"
                    class="triangle-btn"
                  >
                    <a>
                      <span class="triangle text-white majalla32">{{
                        item.id
                      }}</span>
                    </a>
                    <span class="triangle-text p-2 majalla32">{{
                      item.text
                    }}</span>
                  </li>
                </ul>
              </div>
            </div>
            <div class="col-6 text-center">
              <div class="wraper">
                <ul class="btn-wraper">
                  <li
                    v-for="item in section1.slice(2, 4)"
                    :key="item.id"
                    class="triangle-btn"
                  >
                    <a class="">
                      <span class="triangle majalla32">{{ item.id }}</span>
                    </a>
                    <span class="triangle-text p-2 majalla32">{{
                      item.text
                    }}</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="text-center py-5">
            <button
              type="submit"
              @click="scrollToTop" 
              class="btn btn-primary px-5 mt-4 majalla20 blod-none"
            >
              اطلب نسختك الان
            </button>
          </div>
        </div>
      </div>

      <div
        class="row align-items-center justify-content-center text-center padd"
      >
        <div class="col-4 text-int">
          <div class="d-flex align-items-center triangle-item right none">
            <p class="ps-2 ps-3 tops majalla28">لاستهداف صحيح</p>
            <img src="../assets/Arrow1.png" alt="" width="95px" class="none" />
          </div>
          <div class="d-flex align-items-center right none">
            <p class="ps-3 majalla28">لترويج وإقناع قوي</p>
            <img src="../assets/Arrow2.png" alt="" width="95px" height="20px" />
          </div>
          <div class="d-flex align-items-center right none">
            <p class="pt-5 ps-3 majalla28">لمنتج مميز ومقنع للعملاء</p>
            <img src="../assets/Arrow3.png" alt="" width="95px" class="none" />
          </div>
        </div>
        <div class="col-4">
          <div class="box-book">
            <img src="../assets/bok2.png" alt="" />
          </div>
        </div>

        <div class="col-4 text-int">
          <div class="d-flex align-items-center triangle-item right2 none">
            <img src="../assets/Arrow4.png" alt="" width="95px" />
            <p class="pe-3 tops majalla28">لتحديد استراتجية السوق المقنعة</p>
          </div>
          <div class="d-flex align-items-center right2 none">
            <img src="../assets/Arrow6.png" alt="" width="95px" height="20px" />
            <p class="pe-3 majalla28">لجعلك نشاطك قوي</p>
          </div>
          <div class="d-flex align-items-center right2 none">
            <img src="../assets/Arrow5.png" alt="" width="95px" class="" />
            <p class="pt-5 pe-3 bott majalla28">لزيادة مبيعات</p>
          </div>
        </div>
      </div>

      <div class="showmobile pb-5">
        <div class="row">
          <div class="col-12">
            <div class="box-book mob-img">
              <img src="../assets/bok2.png" alt="" />
            </div>
          </div>
          <div class="col-6">
            <div>
              <div class="d-flex align-items-center justify-content-center">
                <img src="../assets/circle.png" alt="" width="40px" />
                <p class="majalla28">استهداف صحيح</p>
              </div>
              <div class="d-flex align-items-center justify-content-center">
                <img src="../assets/circle.png" alt="" width="40px" />
                <p class="majalla28">استهداف صحيح</p>
              </div>
              <div class="d-flex align-items-center justify-content-center">
                <img src="../assets/circle.png" alt="" width="40px" />
                <p class="majalla28">استهداف صحيح</p>
              </div>
            </div>
          </div>
          <div class="col-6">
            <div>
              <div class="d-flex align-items-center justify-content-center">
                <img src="../assets/circle.png" alt="" width="40px" />
                <p class="majalla28">استهداف صحيح</p>
              </div>
              <div class="d-flex align-items-center justify-content-center">
                <img src="../assets/circle.png" alt="" width="40px" />
                <p class="majalla28">استهداف صحيح</p>
              </div>
              <div class="d-flex align-items-center justify-content-center">
                <img src="../assets/circle.png" alt="" width="40px" />
                <p class="majalla28">استهداف صحيح</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      section1: [
        { id: 1, text: "نقدم لكم أفكارنا المجنونة على طبق من ذهب" },
        { id: 2, text: "استهداف صحيح في فعالية اليوم الوطني" },
        { id: 3, text: "استهداف صحيح في فعالية اليوم الوطني" },
        { id: 4, text: "كيف تجعل قابلية أعلى لعملائك" },
      ],
      section3: [
        { text: "استهداف صحيح", image: "../assets/Arrow1.png" },
        { text: "استهداف صحيح", image: "../assets/Arrow2.png" },
        { text: "استهداف صحيح", image: "../assets/Arrow3.png" },
      ],
      section4: [
        { text: "استهداف صحيح", image: "../assets/Arrow4.png" },
        { text: "استهداف صحيح", image: "../assets/Arrow6.png" },
        { text: "استهداف صحيح", image: "../assets/Arrow5.png" },
      ],
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth"
      });
    }
  }
};
</script>

<style>
.triangle-text {
  margin-left: 10px; /* تعديل الهامش بين الشكل والنص حسب الحاجة */
  color: #000; /* لون النص */
  font-weight: bold; /* سمك الخط */
}
.right {
  padding-right: 29%;
}
.right2 {
  padding-left: 29%;
}
.tops {
  margin-top: -50px;
}
.bott {
  margin-top: 6px;
}
</style>