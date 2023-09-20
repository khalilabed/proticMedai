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
      isSubmitting: false, // Add this property to track form submission
      uploading: false,
      successMessage: "",
    };
  },
  methods: {
    async postData() {
      try {
        this.isSubmitting = true;
        const response = await axios.post(
          "http://192.168.3.103/celebration/public/api/send-email-pdf",
          {
            name: this.name,
            email: this.email,
          }
        );
        console.log("Data sent successfully:", response.data);

        // Clear the input fields after successful submission
        this.name = "";
        this.email = "";

        // Show a success message
        this.uploading = true;
        this.successMessage = "تم الاسال بنجاح";

        // Reset isSubmitting, uploading, and successMessage after a certain time if needed
        setTimeout(() => {
          this.isSubmitting = false;
          this.uploading = false;
          this.successMessage = "";
        }, 5000); // Clear the message after 5 seconds (adjust the time as needed)
      } catch (error) {
        console.error("Error sending data:", error);
        // Handle errors as needed
      }
    },
  },
};
</script>
<style>
@import "@/assets/css/styles.css";
</style>