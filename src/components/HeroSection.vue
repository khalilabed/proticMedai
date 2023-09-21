<template>
  <div class="hero-section">
    <div class="container py-5">
      <div class="row d-flex align-items-center">
        <div class="col-md-12 col-lg-6">
          <div class="box-icon img-hero">
            <img src="../assets/box-hero.png" alt="" />
          </div>
          <div class="top-resp">
            <h5 class="py-3 majalla32 text-muted">
              ما لم تخبرك به شركات التسويق
            </h5>
            <div class="d-flex">
              <h2 class="majallab56">
                زد مبيعات متجرك %500 <br />بهذه الاستراتيجيات
                <img src="../assets/icon-hero.png" alt="" width="70px" />
              </h2>
            </div>
          </div>
        </div>
        <div class="col-md-12 col-lg-6">
          <div class="black">
            <h4 class="majallab28 text-center py-2">
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
                      class="form-control majalla20"
                      v-model="name"
                      placeholder="ادخل اسمك هنا"
                    />
                  </div>
                  <div class="my-2">
                    <input
                      type="email"
                      class="form-control majalla20"
                      v-model="email"
                      placeholder="ايميلك الشخصي"
                    />
                  </div>
                  <div class="my-4 but">
                    <button
                      type="submit"
                      class="btn btn-primary majalla20 blod-none"
                      :disabled="isSubmitting"
                    >
                      {{ isSubmitting ? "جاري الإرسال..." : "أطلب نسختك الآن" }}
                    </button>
                    <!-- عرض الرسالة عندما يكون uploading هو true -->
                    <div v-if="uploading" class="text-success majalla18">
                      {{ successMessage }}
                    </div>
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
import axios from "axios";
export default {
  data() {
    return {
      name: "",
      email: "",
      phone: "",
      uploading: false,
      successMessage: "",
    };
  },
  methods: {
    async postData() {
      try {
        const response = await axios.post(
          "https://website.moalhathloul.com/api/send-email-pdf",
          {
            name: this.name,
            email: this.email,
            phone: this.phone,
          }
        );
        console.log("Data sent successfully:", response.data);
        const newTab = window.open(
          "https://drive.google.com/file/d/1gP-FfEl5XW2WLhgAF1UqrIhU0fVr16z9/view?usp=sharing",
          "_blank"
        );
        if (newTab) {
          newTab.focus(); // Optional: Focus on the new tab
        }
        this.name = "";
        this.email = "";
        this.phone = "";
      } catch (error) {
        console.error("Error sending data:", error);
      }
    },
  },
};
</script>
<style>
@import "@/assets/css/styles.css";
</style>