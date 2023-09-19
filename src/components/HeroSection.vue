<template>
  <div class="hero-section">
    <div class="container py-5">
      <div class="row d-flex align-items-center">
        <div class="col-md-12 col-lg-6">
          <div class="box-icon img-hero">
            <img src="../assets/box-hero.png" alt="" />
          </div>
          <div class="top-resp">
            <h5 class="py-3 font-Medium">ما لم تخبرك به شركات التسويق</h5>
            <div class="d-flex">
              <h2 class="">
                زد مبيعات متجرك %500 <br />بهذه الاستراتيجيات
                <img src="../assets/icon-hero.png" alt="" width="50px" />
              </h2>
            </div>
          </div>
        </div>
        <div class="col-md-12 col-lg-6">
          <div class="black">
            <h4 class="font-Regular14 text-center py-2">
              اطلب الكتيب اليوم واحصل على خصم فوري
            </h4>
            <div
              class="row box-input d-flex align-items-center justify-content-center"
            >
              <div class="col-12">
                <form @submit.prevent="postData">
                  <div class="my-2">
                    <input
                      type="text"
                      class="form-control"
                      v-model="name"
                      placeholder="ادخل اسمك هنا"
                    />
                  </div>
                  <div class="my-2">
                    <input
                      type="email"
                      class="form-control"
                      v-model="email"
                      placeholder="ايميلك الشخصي"
                    />
                  </div>
                  <div class="my-2 but">
                    <button
                      type="submit"
                      class="btn btn-primary font-Regular14 blod-none"
                    >
                      أطلب هديتك الفورية
                    </button>
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import axios from "axios";

export default {
  methods: {
    //     async postData() {
    //       try {
    //         const response = await axios.post(
    //           "http://192.168.3.103/celebration/public/api/gifts",
    //           {
    //             name: this.name,
    //             email: this.email,
    //           }
    //         );
    //         console.log("Data sent successfully:", response.data);
    //         const newTab = window.open("https://google.com", "_blank");
    //         if (newTab) {
    //           newTab.focus(); // Optional: Focus on the new tab
    //         }
    //         this.name = "";
    //         this.email = "";
    //       } catch (error) {
    //         console.error("Error sending data:", error);
    //       }
    //     },
  },
};
</script>

<style>
@import "@/assets/css/styles.css";
</style>