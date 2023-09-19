<template>
  <div class="container pt-5">
    <div class="text-center pt-5">
      <h3>مميزات لن تجدها في مكان آخر</h3>
    </div>
    <div class="py-5">
      <div>
        <div class="row">
          <div class="col-lg-6 text-center">
            <div class="wraper">
              <ul class="btn-wraper">
                <li
                  v-for="item in section1.slice(0, 3)"
                  :key="item.id"
                  class="triangle-btn"
                >
                  <a>
                    <span class="triangle text-white">{{ item.id }}</span>
                  </a>
                  <span class="triangle-text p-2">{{ item.text }}</span>
                </li>
              </ul>
            </div>
          </div>
          <div class="col-lg-6 text-center">
            <div class="wraper">
              <ul class="btn-wraper">
                <li
                  v-for="item in section1.slice(3, 5)"
                  :key="item.id"
                  class="triangle-btn"
                >
                  <a class="">
                    <span class="triangle">{{ item.id }}</span>
                  </a>
                  <span class="triangle-text p-2">{{ item.text }}</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row align-items-center justify-content-center text-center py-5">
      <div class="col-lg-3 col-md-12">
        <div class="d-flex align-items-center triangle-item right none">
          <p class="ps-2 ps-3 tops ">استهداف صحيح</p>
          <img src="../assets/Arrow1.png" alt="" width="95px" class="none" />
        </div>
        <div class="d-flex align-items-center right none">
          <p class="ps-3">استهداف صحيح</p>
          <img src="../assets/Arrow2.png" alt="" width="95px" height="20px"   />
        </div>
        <div class="d-flex align-items-center right none">
          <p class="pt-5 ps-3">استهداف صحيح</p>
          <img src="../assets/Arrow3.png" alt="" width="95px" class="none" />
        </div>
      </div>
      <div class="col-lg-6 col-md-12">
        <div class="box-book">
          <img src="../assets/books3.png" alt=""  />
        </div>
      </div>

      <div class="col-lg-3 col-md-12">
        <div class="d-flex align-items-center triangle-item right2 none">
          <img src="../assets/Arrow4.png" alt="" width="95px"  />
          <p class="pe-3 tops">استهداف صحيح</p>
        </div>
        <div class="d-flex align-items-center right2 none">
          <img src="../assets/Arrow6.png" alt="" width="95px" height="20px"  />
          <p class="pe-3">استهداف صحيح</p>
        </div>
        <div class="d-flex align-items-center right2 none" >
          <img src="../assets/Arrow5.png" alt="" width="95px" class=""  />
          <p class="pt-5 pe-3 bott">استهداف صحيح</p>
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
        { id: 1, text: "استهداف صحيح" },
        { id: 2, text: "استهداف صحيح" },
        { id: 3, text: "استهداف صحيح" },
        { id: 4, text: "استهداف صحيح" },
        { id: 5, text: "استهداف صحيح" },
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
};
</script>

<style>
.triangle-text {
  margin-left: 10px; /* تعديل الهامش بين الشكل والنص حسب الحاجة */
  color: #000; /* لون النص */
  font-weight: bold; /* سمك الخط */
}
.right {
  padding-right: 29%
}
.right2 {
  padding-left: 29%;
}
.tops{
    margin-top: -50px;
}
.bott{
    margin-top: 6px;
}
</style>